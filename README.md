# USB_VCP_test_on_STM32F4Discovery_board

A minimal CubeMX generated setup for a STM32F4DISCOVERY board with USB VCP Hello World code.
On MacOS.
Compile with GCC and flash with OpenOCD. Suggest installing these with Homebrew.
If you don't have Homebrew installed you can get it with:
```
/usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
```

Install OpenOCD with:
```
brew install openocd
```

Install GCC with: (edit:see note below)
```
brew cask install gcc-arm-embedded
```
edit (February 26th, 2019): the 'gcc-arm-embedded' cask may be gone again. A work around was posted on
https://github.com/Homebrew/homebrew-cask/pull/56802
which is:
```
brew cask install https://raw.githubusercontent.com/Homebrew/homebrew-cask/b88346667547cc85f8f2cacb3dfe7b754c8afc8a/Casks/gcc-arm-embedded.rb
```


In Terminal change directory this folder and run ``sh openocd`` (alternatively ``./openocd``, but you might have to run ``chmod +x openocd`` first to give the openocd shellscript executive permissions first).
Open another terminal window, same folder, and run ``make clean``. Then run ``make flash``.
Open a serial console (e.g. the console in the Arduino IDE) and check if you can connect to the serial port the board generated.
