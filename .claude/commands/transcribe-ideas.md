Process all audio files in the to-process/ folder using the following workflow:

1. Find all audio files (*.mp3, *.m4a, *.wav, *.ogg, *.flac) in the to-process/ folder
2. For each audio file:
   - Use the AssemblyAI MCP to transcribe the audio file
   - Create a descriptive folder name based on the content (infer from transcript)
   - Create a new folder in pending/ with that name
   - Move the original audio file into that folder
   - Save the raw transcript as "transcript-raw.md" with the current date at the top
   - Create a refined version of the transcript as "transcript-refined.md" (clean up filler words, improve readability, but preserve all content and intent)
   - Add the current date to the top of both transcript files

3. After processing all files, provide a summary of:
   - How many audio files were processed
   - The folder names created
   - Any errors or issues encountered

Important notes:
- Always preserve the original audio file
- The raw transcript must remain unchanged from the MCP output (except for adding the date)
- The refined transcript should improve readability while preserving all details
- Use descriptive folder names (e.g., "pipewire-source-priority-organiser" not "idea-1")
- If no audio files are found in to-process/, inform the user and exit gracefully
