## Claude Code Stop Sound

Get audio notifications when Claude Code finishes running tasks on macOS and Windows, add this hook to your Claude Code settings file:

- **Global**: `~/.claude/settings.json`
- **Project**: `.claude/settings.json`

### macOS
```json
{
  "hooks": {
    "Stop": [
      {
        "matcher": "",
        "hooks": [
          {
            "type": "command",
            "command": "afplay /System/Library/Sounds/Glass.aiff"
          }
        ]
      }
    ]
  }
}
```

### Windows
```json
{
  "hooks": {
    "Stop": [
      {
        "matcher": "",
        "hooks": [
          {
            "type": "command",
            "command": "powershell -c \"(New-Object Media.SoundPlayer 'C:\\Windows\\Media\\Windows Notify System Generic.wav').PlaySync()\""
          }
        ]
      }
    ]
  }
}
```