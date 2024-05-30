- Install [Gradle](https://gradle.org/install/)
- Install [Google Cloud Command Line Interface (CLI)](https://cloud.google.com/sdk/docs/install)
    - At end of install, let installer log in to your Google account
    - Choose cloud project to use
- Open CLI and run `gcloud beta services api-keys create --display-name GOOGLE-API-KEY`
- The output from this command will have `"keyString":"<your Keystring Value>",`
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

