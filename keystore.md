# keystore

Keystores contain certificate information that contains security information and is used when publishing apps to Android market.

A "keystore" is a database used by JDK "keytool" command and KeyStore class to store your own private keys, and public key certificates you received from others. "keystore" supports the following features:

* Two types of entries: key entries for private keys and certificate entries for public key certificates.
* A key entry contains the private key and a certificate chain of the corresponding public key.
* Every entry has a unique alias name.
* Key entries are protected by separate passwords.
* "keystore" may have different implementations from different security package providers. The default implementation from Sun is called JKS \(Java Key Store\).

##### Creation

A keystore is created when you initially create your first app. Every AI distribution contains its own unique keystore. As result, **if you have published an app **from another repository \(e.g. MIT AI\), and now would like to continue with AppyBuilder, you'll have to import keystore from MIT AI into AppyBuilder.

_**NOTE: Before performing any imports, create a backup of your existing keystore by exporting it. Otherwise, you may encounter issues when you try to publish apps into Android market.**_

The export / import can be done by selecting Projects menu, then selecting "Export keystore" or "Import keystore"

![](http://community.appybuilder.com/uploads/default/original/1X/522f5c637576f04f63471d829a9bf15e83a3a927.png)



.

