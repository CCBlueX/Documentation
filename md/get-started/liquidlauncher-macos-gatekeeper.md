# Running LiquidLauncher on macOS

## About the "App is damaged" Warning

On macOS (especially on Apple Silicon Macs like M1, M2 or M3), you may see this message when you open LiquidLauncher:

> "LiquidLauncher" is damaged and can't be opened. You should move it to the trash.

The app is not broken. macOS shows this because LiquidLauncher is not signed with an Apple developer certificate, which costs $99 a year and which we do not have.

## How to Fix the Issue

macOS marks every app you download from the internet as "quarantined". You can remove that mark with one Terminal command.

### Method 1: Using Terminal Command

1. Install the app by dragging it to your Applications folder as usual
2. Open Terminal (you can find it in Applications > Utilities > Terminal)
3. Copy and paste the following command:

```bash
xattr -d com.apple.quarantine /Applications/LiquidLauncher.app
```

4. Press Enter to execute the command
5. Try launching LiquidLauncher again

### What Does This Command Do?

It removes the quarantine mark from LiquidLauncher, so macOS stops showing the warning.

- `xattr` shows and changes extra information stored on files
- `-d` deletes one piece of that information
- `com.apple.quarantine` is the mark that says the file came from the internet
- `/Applications/LiquidLauncher.app` is where LiquidLauncher is installed

### Method 2: System Preferences

You can also try allowing the app through System Preferences:

1. Go to System Preferences > Security & Privacy
2. On the General tab, you might see a message about LiquidLauncher being blocked
3. Click "Open Anyway" to override the security check

This does not always work for unsigned apps, so try the Terminal command first.

## Is This Safe?

Yes, as long as you downloaded LiquidLauncher from our website or our GitHub page. The quarantine mark is there to stop apps you did not mean to open. You downloaded LiquidLauncher on purpose, so removing it is fine.