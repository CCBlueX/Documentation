# Running LiquidLauncher on macOS

## About the "App is damaged" Warning

When downloading and running LiquidLauncher on macOS (especially on Apple Silicon Macs like M1/M2/M3), you may encounter an error message that says:

> "LiquidLauncher" is damaged and can't be opened. You should move it to the trash.

This message appears because LiquidLauncher is not signed with an Apple Developer certificate. Apple requires applications to be signed with a paid developer certificate ($99/year) to run without warnings, which is something we currently don't provide.

## How to Fix the Issue

To fix this issue, you'll need to remove the quarantine attribute that macOS adds to downloaded applications. This can be done with a simple Terminal command.

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

The `xattr -d com.apple.quarantine` command removes the quarantine attribute that macOS automatically adds to applications downloaded from the internet. This attribute is what causes macOS to display the warning message.

- `xattr`: This command is used to display and manipulate extended attributes of files
- `-d`: This flag tells xattr to delete an attribute
- `com.apple.quarantine`: This is the specific attribute that marks the file as downloaded from the internet
- `/Applications/LiquidLauncher.app`: This is the path to the LiquidLauncher application

### Method 2: System Preferences (Less Recommended)

You can also try allowing the app through System Preferences:

1. Go to System Preferences > Security & Privacy
2. On the General tab, you might see a message about LiquidLauncher being blocked
3. Click "Open Anyway" to override the security check

**Note:** This method may not always work for unsigned applications, which is why the Terminal command is the recommended solution.

## Is This Safe?

Yes, this is safe as long as you've downloaded LiquidLauncher from our official website or GitHub repository. The quarantine attribute is a security feature designed to prevent unknown applications from running, but since you've intentionally downloaded our application, it's safe to bypass in this case.

We're working on improving our macOS support, but until then, this workaround will let you use LiquidLauncher on all macOS systems including Apple Silicon Macs.