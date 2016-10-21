# Frame-SDK
Open source environmental monitoring platform, consisting of arduino-compatible hardware, data visualization, web and mobile app, and full featured API.

Hardware involved
- Motor common thread with 4 relays controlled by A/D, PWM for light control
- Arduino-compatible board with environmental sensor (Lux, Humidity, CO, Temp, ...)
- Wi-Fi connection for interoperability via HTTP interface

Software included
- FrameMonitor-bin: hood emulator, consist in an Win-executable made in Framework.NET, in order to test the Frame SDK
- FrameApp-bin: apk for Android
- FrameApp-src: src of app Android, made in Xamarin.Android C#
