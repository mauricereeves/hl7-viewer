# hl7-viewer

## Purpose
This project was created to allow for the reading and viewing of the information in an HL7 message.
HL7 messages are generally noisy and verbose, with nested delimited fields that align with a versioned spec.
Manually reading the messages can be daunting at first, which is what this project attempts to address.

## Example
Below is an example of an HL7 message, using faked information
```
FHS|^~\&|CDC PRIME - Atlanta, Georgia (Dekalb)^2.16.840.1.114222.4.1.237821^ISO|CDC PRIME - Atlanta, Georgia (Dekalb)^2.16.840.1.114222.4.1.237821^ISO|0.0.0.0.1|0.0.0.0.1|202101051614-0500
BHS|^~\&|CDC PRIME - Atlanta, Georgia (Dekalb)^2.16.840.1.114222.4.1.237821^ISO|CDC PRIME - Atlanta, Georgia (Dekalb)^2.16.840.1.114222.4.1.237821^ISO|0.0.0.0.1|0.0.0.0.1|202101051614-0500
MSH|^~\&|CDC PRIME - Atlanta, Georgia (Dekalb)^2.16.840.1.114222.4.1.237821^ISO|Any facility USA^32D2156308^CLIA|0.0.0.0.1|0.0.0.0.1|20210105161431.856-0500||ORU^R01^ORU_R01|310101|D|2.5.1|||NE|NE|USA
SFT|Centers for Disease Control and Prevention|0.1-SNAPSHOT|PRIME Data Hub|0.1-SNAPSHOT||20210105
PID|1||||Rau^Jesusita^Jenni||19870502|A||2054-5^Black or African American^HL70005^^^^2.5.1|4704 Hermiston Groves^^Port Changside^PA^15597||^PRN^^^1^249^2644870
ORC|RE||638570||||||||||||||||||Any facility USA|598 Hahn Drives^^Dickibury^PA^77889||155 Sean Springs^^Kennytown^PA^79819
OBR|1||638570||||202012292231-0500|202012292231-0500
OBX|1|CWE||||||||||||202012292231-0500
NTE|||ijci37zj|RE^Remark^HL70364^^^^2.5.1
SPM|1|||871810001^Mid-turbinate nasal swab^SCT||||71836000^Nasopharyngeal structure (body structure)^SCT^^^^2020-09-01|||||||||202012292231-0500^202012292231-0500|202101020108-0500
BTS|1
FTS|1
```

## Running
The HL7 Viewer app is a simple Node.js application running as a static website, using JS to parse and
display the information. It utilizes Bootstrap and jQuery in order to parse and dynamically add elements to the DOM. This wasn't done because I'm married to jQuery or other technologies from bygone eras. This was just to get up to speed quickly. This would probably benefit from using ReactJS or some other more modern powerful framework.

