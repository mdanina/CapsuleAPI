# Windows
To build with CMake use the following:
```bash
cd Example/Win
cmake -S . -B ./build -G "Visual Studio 17 2022" -A x64
cmake --build ./build --config Release
```

# MacOS
You may be prompted to grant permissions for unknown library `libCapsuleClient.dylib`.

This is a normal behavior, you can sign your app later.

For Apple Silicon CPU based devices run this command:
```zsh
arch -x86_64 zsh
```
and then proceed as usual.

To build with CMake use the following:
```bash
cd Example/Mac
cmake -S . -L ./build/libCapsuleClient.dylib -B ./build -G  "Xcode"
cmake --build ./build --config Release
```

# Description

Abovementioned commands will build several example executables. Here's their description and usage. 

## Client Example

This example shows how to use basic features of Capsule C API.

### Usage

To run this example, `cd` to the directory, where examples were built and run the following command:

```bash
./CapsuleClientExample --key=<YOUR_LICENSE_KEY>
```
This example accepts an optional argument:

- `--key=<LICENSE_KEY>` - license key without quotes

You can omit the `--key` argument. In that case the program will ask you to enter the key during execution.

To **quit** the example enter `q` or `Q` key and press enter.

## Raw Signal Example

This example shows how to get raw signal data (EEG, PPG and MEMS) from a device using C API.

### Usage

To run this example, `cd` to the directory, where examples were built and run the following command:

```bash
./CapsuleRawSignalExample --csv=[true/false]
```

This example accepts an optional argument:

- `--csv=<BOOL>` - write signal data to a csv file. It accepts `[true, on, 1]` for **true** and `[false, off, 0]` for **false**

You can omit the argument. In that case the program will ask you to choose the setting during execution.

To **quit** the example enter `q` or `Q` key and press enter.

## Filtered Signal Example

This signal shows how to get filtered EEG signal in bipolar or monopolar mode using C API.

### Usage

To run this example, `cd` to the directory, where examples were built and run the following command:

```bash
./CapsuleFilteredSignalExample --key=<LICENSE_KEY> --bipolar=[true/false] --csv=[true/false]
```

This example accepts 3 arguments:

- `--key=<LICENSE_KEY` - license key withou quotes
- `--bipolar=<BOOL>` - run session in bipolar or monopolar mode. It accepts `[true, on, 1]` for **true** and `[false, off, 0]` for **false**
- `--csv=<BOOL>` - write signal data to a csv file. It accepts `[true, on, 1]` for **true** and `[false, off, 0]` for **false**

You can omit some arguments. In that case the program will ask you to choose these settings during execution.

To **quit** the example enter `q` or `Q` key and press enter.
