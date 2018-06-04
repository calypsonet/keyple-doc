# 'Eclipse Keyple' project 
## Status & current works (18/06/05)
- **Week #22**:
  - Finished a wide refactoring of the SE Proxy layer to requests for multi-SE.
  - Two PC Java examples are fully ready for the PC/SC plugin:
    - KeypleGenericDemo_ObservableReaderNotification ( https://github.com/calypsonet/keyple-java/blob/develop/keyple-example-pc/src/main/java/org/eclipse/keyple/examples/pc/KeypleGenericDemo_ObservableReaderNotification.java ) => to observe the readers' configuration & SEs' status on a PC (notification of reader hot-plug/unplug, notification of SE insertion/removal).
    - KeypleGenericDemo_SeProtocolDetection ( https://github.com/calypsonet/keyple-java/blob/develop/keyple-example-pc/src/main/java/org/eclipse/keyple/examples/pc/KeypleGenericDemo_SeProtocolDetection.java ) => to detect the kind of SE presented on a contactless reader.

- **Week #23**:
  - Update of the Calypso Secured Session (org.eclipse.keyple.calypso.transaction.PoSecureSession) in order to support the new multi-SE request feature.
    - The third PC Java example 'KeypleCalypsoDemo_HoplinkTransaction' (operation a Calypso Secure Session in case a **Hoplink** test card is detected) will be fixed to support the multi-SE feature.
  - Improvements org.eclipse.keyple.seproxyAbstractObservableReader (to provide generic logging of SeRequest/SeResponse) and 
org.eclipse.keyple.seproxy.AbstractLocalReader (to factorize as possible the ApduRequest/ApduResponse processing between plugins of local readers).
- June 2018
  - Definition of the Remote SE plugin.

## Documentations & binaries
### Functional specifications:

 - **'Keyple Core module' specification**': https://calypsonet.github.io/keyple-doc/keyple-core-spec/ 
   - => since a recent refactoring the text of the chapters §2.2 & §2.3 has still to be rewritten but all the related UML class diagrams are inline with the current java implementation.
   - **'Keyple Calypso Library specification'**: https://calypsonet.github.io/keyple-doc/keyple-extension-calypso-spec/

### JavaDoc{s}
- **'Keyple Core module' JavaDoc**: https://calypsonet.github.io/keyple-java/develop/keyple-core/javadoc/
 - **'Keyple Calypso Library JavaDoc'**: https://calypsonet.github.io/keyple-java/develop/keyple-calypso/javadoc/
 - **'Keyple plugin PC/SC JavaDoc'**: https://calypsonet.github.io/keyple-java/develop/keyple-plugin-pcsc/javadoc/index.html
https://calypsonet.github.io/keyple-java/develop/keyple-plugin-stub/javadoc/
- **'Keyple plugin PC "stub" JavaDoc'**: https://calypsonet.github.io/keyple-java/develop/keyple-plugin-stub/javadoc/

For the moment, the JavaDocs of the two Android plugins (NFC reader & OMAPI) aren't yet publicly hosted on github.io => it'll be solved in the coming weeks. Pending, developers have the possibility to generate them by themselves from the keyple-java repository.
 
### JARs
 Simple archives:
- **'Keyple Core module' JAR**:  https://calypsonet.github.io/keyple-java/develop/jars/keyple-core-1.0-SNAPSHOT.jar
 - **'Keyple Calypso Library JAR'**: https://calypsonet.github.io/keyple-java/develop/jars/keyple-calypso-1.0-SNAPSHOT.jar
 - **'Keyple plugin PC/SC JAR'**: https://calypsonet.github.io/keyple-java/develop/jars/keyple-plugin-pcsc-1.0-SNAPSHOT.jar
- **'Keyple plugin PC "stub" JAR'**: https://calypsonet.github.io/keyple-java/develop/jars/keyple-plugin-stub-1.0-SNAPSHOT.jar

For the moment, the JARs of the two Android plugins (NFC reader & OMAPI) aren't yet publicly hosted on github.io => it'll be solved in the coming weeks.

Fat archive:
- **'FAT JAR of PC examples with dependencies'**: https://calypsonet.github.io/keyple-java/develop/jars/keyple-example-pc-1.0-SNAPSHOT.jar