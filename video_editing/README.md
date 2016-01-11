### Audio
1. `ffmpeg -i INPUTVIDEO -acodec libmp3lame -metadata TITLE="TITLE" FILENAME.mp3`
2. Adacity
  1. Noise removal 2x
  2. Normalize
  3. Compress
3. Replace Audio
  - `ffmpeg -i AUDIOFILE -i VIDEOFILE -acodec copy -vcodec copy OUTPUTNAME`
