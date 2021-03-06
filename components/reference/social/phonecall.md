# PhoneCall

A non-visible component that makes a phone call to the number specified in the PhoneNumber property, which can be set either in the Designer or Blocks Editor. The component has a MakePhoneCall method, enabling the program to launch a phone call.

Often, this component is used with the ContactPicker component, which lets the user select a contact from the ones stored on the phone and sets the PhoneNumber property to the contact's phone number.

To directly specify the phone number (e.g., 650-555-1212), set the PhoneNumber property to a Text with the specified digits (e.g., "6505551212"). Dashes, dots, and parentheses may be included (e.g., "(650)-555-1212") but will be ignored; spaces may not be included.

---

### Properties

#### PhoneNumber

---

### Events

#### IncomingCallAnswered(text phoneNumber)

Event indicating that an incoming phone call is answered. phoneNumber is the incoming call phone number.

#### PhoneCallEnded(number status, text phoneNumber)

Event indicating that a phone call has ended. If status is 1, incoming call is missed or rejected; if status is 2, incoming call is answered before hanging up; if status is 3, outgoing call is hung up. phoneNumber is the ended call phone number.

#### PhoneCallStarted(number status, text phoneNumber)

Event indicating that a phonecall has started. If status is 1, incoming call is ringing; if status is 2, outgoing call is dialled. phoneNumber is the incoming/outgoing phone number.

---

### Methods

#### MakePhoneCall()

Makes a phone call using the number in the PhoneNumber property.
