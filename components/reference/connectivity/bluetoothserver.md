# BluetoothServer

Picture of Bluetooth Server component

Bluetooth server component

---

### Properties

#### Available

Tell whether Bluetooth is available on the Android device.

#### CharacterEncoding

The character encoding to use when sending and receiving text.

#### DelimiterByte

The delimiter byte to use when passing a negative number for the numberOfBytes parameter when calling ReceiveText, ReceiveSignedBytes, or ReceiveUnsignedBytes.

#### Enabled

Tell whether Bluetooth is enabled.

#### HighByteFirst

Whether 2 and 4 byte numbers should be sent and received with the high (or most significant) byte first. Check the documentation for the device with which your app will be communicating for the appropriate setting. This is also known as big-endian.

#### IsAccepting

Tell whether this BluetoothServer component is accepting an incoming connection.

#### IsConnected

Tell whether a Bluetooth connection has been made.

---

### Events

#### ConnectionAccepted()

Indicates that a bluetooth connection has been accepted.

---

### Methods

#### AcceptConnection(text serviceName)

Accept an incoming connection with the Serial Port Profile (SPP).

#### AcceptConnectionWithUUID(text serviceName, text uuid)

Accept an incoming connection with a specific UUID.

#### BytesAvailableToReceive()

Returns an estimate of the number of bytes that can be received without blocking

#### Disconnect()

Disconnect from the connected Bluetooth device.

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

#### StopAccepting()

Stop accepting an incoming connection.
