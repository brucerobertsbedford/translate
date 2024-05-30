- Install [Gradle](https://gradle.org/install/)
- Install [Google Cloud Command Line Interface (CLI)](https://cloud.google.com/sdk/docs/install)
    - At end of install, let installer log in to your Google account
    - Choose cloud project to use
- Open CLI and run `gcloud beta services api-keys create --display-name GOOGLE-API-KEY`
      - You'll get back something that looks like this:
  
  ```
  Operation [operations/akmf.p7-140425901528-a4a63632-8f9a-4815-bd10-72d690ad5ba9] complete. Result: {
    "@type":"type.googleapis.com/google.api.apikeys.v2.Key",
    "createTime":"2024-05-30T10:28:29.680827Z",
    "displayName":"GOOGLE-API-KEY",
    "etag":"W/\"AoQY/WpENvAV1DSSLIVHDQ==\"",
    "keyString":"AIzaSyBqOsroRCPja0SF_H0sK9r8IwEm8uOIs0E",
    "name":"projects/140425901528/locations/global/keys/786a81e0-4d77-45e8-9c7d-959b9d85ec44",
    "uid":"786a81e0-4d77-45e8-9c7d-959b9d85ec44",
    "updateTime":"2024-05-30T10:28:29.721123Z"
- Copy the "keyString" value to the clipboard
- Open a normal DOS shell
- Set the Google API Key into your enviroment:  `set GOOGLE_API_KEY=<your keyString value>`
- Copy this project to your local system.
- Run `go.bat` at the root of this project to test it.  You should see this:
```
C:\Users\bruce\eclipse-workspace\translate>go
C:\Users\bruce\eclipse-workspace\translate>gradle run --args="detect 'my word'"
> Task :app:run
Detected language is:
Detection{language=en, confidence=1.0}
BUILD SUCCESSFUL in 1s
2 actionable tasks: 1 executed, 1 up-to-date
C:\Users\bruce\eclipse-workspace\translate>
```

