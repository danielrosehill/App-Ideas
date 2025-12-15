# Workflow Structure

This repository uses a structured folder system to manage the app ideas pipeline from capture to implementation.

## Folder Structure

```
App-Ideas/
├── to-process/     # Audio files waiting to be transcribed
├── pending/        # Transcribed ideas awaiting refinement or implementation
└── done/           # Completed/implemented ideas
```

## Workflow Process

### 1. Capture (to-process/)
- Record idea as audio file
- Place audio file in `to-process/` folder
- Audio files here trigger the transcription workflow

### 2. Transcribe & Organize (pending/)
- Audio files are transcribed using AssemblyAI MCP or local Whisper
- Each idea gets its own folder in `pending/` with:
  - Original audio file
  - Raw transcript
  - Refined transcript
  - Generated spec (when ready)

### 3. Implement & Archive (done/)
- Once implemented, the idea folder moves to `done/`
- Preserves all context (audio, transcripts, specs)

## Automation

Use the `/transcribe-ideas` slash command to automatically:
1. Find audio files in `to-process/`
2. Transcribe them via AssemblyAI MCP
3. Create organized folders in `pending/`
4. Generate raw and refined transcripts
5. Add timestamps to all transcripts

## Notes

- Audio files are deliberately committed to version control
- Raw transcripts are always preserved alongside refined versions
- Edited audio (silence removal, etc.) replaces originals but maintains context
- Common idea themes can be grouped into subfolders as the repository grows
