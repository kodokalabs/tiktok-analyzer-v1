# TikTok Analyzer
This project was created to show how you can crawl videos from TikTok and convert speech (coming from video) to text.

Used libraries:
* https://github.com/Russell-Newton/TikTokPy
* https://github.com/openai/whisper

You need to clone the repository or download zipped project to run it.
```
git clone https://github.com/data-hunters/tiktok-analyzer.git
```
In next step, install required libraries:
```
pip install tiktokapipy
python -m playwright install
pip install whisper-openai
```

## Examples

Displaying help:
```
python run.py --help
```
<br />

Downloading 10 latest videos (with soundtrack) by hashtag `ukraine` to `tiktok_videos` directory:
```
python run.py --hashtag ukraine --output-path tiktok_videos --max-videos 10
```
<br />

Downloading 10 latest videos (with soundtrack) of `test123` user to `tiktok_videos` directory:
```
python run.py --user test123 --output-path tiktok_videos --max-videos 10
```
<br />

Converting speech to text based on `mp3` files located in `tiktok_videos`, using OpenAI Whisper `medium` model and saving the output to `tiktok_transcription` directory:
```
python run.py --transcribe --input-path tiktok_videos --output-path tiktok_transcription --model medium
```
<br />

Running all of the above steps with single command:
```
python run.py --hashtag ukraine --user test123 --max-videos 10 --transcribe --input-path tiktok_videos --output-path tiktok_videos --model medium
```
  
<br />
<br />  

[![kōdōkalabs](https://kodokalabs.com/wp-content/uploads/2024/06/2024-kodokalabs-logo-color-bg-trans-900-white-font.png)](https://kodokalabs.com)
