# arcsight2win

Support for Windows security events forwarded to splunk by ArcSight as CEF formatted logs.
The props.conf was created to work in conjunction with the official splunk Windows TA.
Validated to work with the CIM Authentication data model

*Prerequisites:*

1. source transformed to WinEventLog:Security (RegEx for Raw events: CEF:0|Microsoft|Microsoft Windows||Microsoft-Windows-Security-auditing)
2. sourcetype transformed to WinEventLog:arcsight
3. Modify locally the eventtypes.conf of TA-win to include sourcetype=WinEventLog:arcsight in [windows_event_signature]

