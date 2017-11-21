# Workflow

- Make Recording
- Digitize (audiorecorder,96/24)
- Make FLAC (embed metadata and location picture/map)
- Make Opus
- Upload to IA

## Coding History Example
A=ANALOGUE,M=stereo,T=Sony TC-D5 PROII; 1 7/8 ips; Compact Cassette; Recording; A=ANALOGUE,M=stereo,T=Akai GX-M50; SN50122-01257 7/8 ips; Compact Cassette; Playback; A=PCM,F=96000,W=24,M=stereo,T=Zoom; UAC-2; SN006082; AD; A=FLAC,F=96000,W=24,M=stereo,T=flac 1.3.2; Encoding

## Location metadata
'LOCATION'  ISO 6709 (to five decimals, minus trailing slash) Example: +40.81013-073.94758

## FLAC Creation Command
flac --best --keep-foreign-metadata --preserve-modtime --verify input.wav

## FLAC embed metadata example commands
`metaflac --import-picture-from="13||||/Users/weevz/Desktop/HarlemRain.jpg" /Users/weevz/Desktop/HarlemRain.flac`

`metaflac --set-tag=SOURCEMEDIA="A=ANALOGUE,M=stereo,T=Sony TC-D5 PROII; 1 7/8 ips; Compact Cassette" --set-tag=LOCATION="+40.81013-073.94758" --set-tag=DATE="2017-03-18 (recorded)" --set-tag=LICENSE="CC BY 4.0 Attribution : Andrew Weaver" --import-picture-from="13||||/input.jpg" input.flac`
