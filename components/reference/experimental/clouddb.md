# CloudDB

Non-visible component allowing you to store data on a Internet connected database server (using Redis software). This allows the users of your App to share data with each other. By default data will be stored in a server maintained by AppyBuilder, however you can setup and run your own server. Set the "RedisServer" property and "RedisPort" Property to access your own server.

---

### Properties

#### ProjectID

Gets the ProjectID for this CloudDB project.

#### RedisPort

The Redis Server port to use. Defaults to 6381

#### RedisServer

The Redis Server to use to store data. A setting of "DEFAULT" means that the MIT server will be used.

#### Token (designer only)

This field contains the authentication token used to login to the backed Redis server. For the "DEFAULT" server, do not edit this value, the system will fill it in for you. A system administrator may also provide a special value to you which can be used to share data between multiple projects from multiple people. If using your own Redis server, set a password in the server's config and enter it here.

#### UseSSL (designer only)

Set to true to use SSL to talk to CloudDB/Redis server. This should be set to True for the "DEFAULT" server.

---

### Events

#### CloudDBError(text message)

Indicates that an error occurred while communicating with the CloudDB Redis server.

#### DataChanged(text tag, any value)

Indicates that the data in the CloudDB project has changed. Launches an event with the tag and value that have been updated.

#### FirstRemoved(any value)

Event triggered by the "RemoveFirstFromList" function. The argument "value" is the object that was the first in the list, and which is now removed.

#### GotValue(text tag, any value)

Indicates that a GetValue request has succeeded.

#### TagList(list value)

Event triggered when we have received the list of known tags. Used with the "GetTagList" Function.

---

### Methods

#### AppendValueToList(text tag, any itemToAdd)

Append a value to the end of a list atomically. If two devices use this function simultaneously, both will be appended and no data lost.

#### ClearTag(text tag)

Remove the tag from CloudDB

#### CloudConnected()

returns True if we are on the network and will likely be able to connect to the CloudDB server.

#### GetTagList()

Get the list of tags for this application. When complete a "TagList" event will be triggered with the list of known tags.

#### GetValue(text tag, any valueIfTagNotThere)

GetValue asks CloudDB to get the value stored under the given tag. It will pass valueIfTagNotThere to GotValue if there is no value stored under the tag.

#### RemoveFirstFromList(text tag)

Return the first element of a list and atomically remove it. If two devices use this function simultaneously, one will get the first element and the the other will get the second element, or an error if there is no available element. When the element is available, the "FirstRemoved" event will be triggered.

#### StoreValue(text tag, any valueToStore)

Asks CloudDB to store the given value under the given tag.
