# BluetoothClient

Bluetooth client component

---

### Properties

#### AddressesAndNames

The addresses and names of paired Bluetooth devices

#### Available

Whether Bluetooth is available on the device

#### CharacterEncoding

#### DelimiterByte

#### Enabled

Whether Bluetooth is enabled

#### HighByteFirst

#### IsConnected

#### Secure

Whether to invoke SSP (Simple Secure Pairing), which is supported on devices with Bluetooth v2.1 or higher. When working with embedded Bluetooth devices, this property may need to be set to False. For Android 2.0-2.2, this property setting will be ignored.

---

### Events

none

---

### Methods

#### BytesAvailableToReceive()

Returns an estimate of the number of bytes that can be received without blocking

#### Connect(text address)

Connect to the Bluetooth device with the specified address and the Serial Port Profile (SPP). Returns true if the connection was successful.

#### ConnectWithUUID(text address, text uuid)

Connect to the Bluetooth device with the specified address and UUID. Returns true if the connection was successful.

#### Disconnect()

Disconnect from the connected Bluetooth device.

#### IsDevicePaired(text address)

Checks whether the Bluetooth device with the specified address is paired.

#### ReceiveSigned1ByteNumber()

Receive a signed 1-byte number from the connected Bluetooth device.

#### ReceiveSigned2ByteNumber()

Receive a signed 2-byte number from the connected Bluetooth device.

#### ReceiveSigned4ByteNumber()

Receive a signed 4-byte number from the connected Bluetooth device.

#### ReceiveSignedBytes(number numberOfBytes)

Receive multiple signed byte values from the connected Bluetooth device. If numberOfBytes is less than 0, read until a delimiter byte value is received.

#### ReceiveText(number numberOfBytes)

Receive text from the connected Bluetooth device. If numberOfBytes is less than 0, read until a delimiter byte value is received.

#### ReceiveUnsigned1ByteNumber()

Receive an unsigned 1-byte number from the connected Bluetooth device.

#### ReceiveUnsigned2ByteNumber()

Receive a unsigned 2-byte number from the connected Bluetooth device.

#### ReceiveUnsigned4ByteNumber()

Receive a unsigned 4-byte number from the connected Bluetooth device.

#### ReceiveUnsignedBytes(number numberOfBytes)

Receive multiple unsigned byte values from the connected Bluetooth device. If numberOfBytes is less than 0, read until a delimiter byte value is received.

#### Send1ByteNumber(text number)

Send a 1-byte number to the connected Bluetooth device.

#### Send2ByteNumber(text number)

Send a 2-byte number to the connected Bluetooth device.

#### Send4ByteNumber(text number)

Send a 4-byte number to the connected Bluetooth device.

#### SendBytes(list list)

Send a list of byte values to the connected Bluetooth device.

#### SendText(text text)

Send text to the connected Bluetooth device.
