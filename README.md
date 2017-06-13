# Workflow

- Make Recording
- Digitize (audiorecorder,96/24)
- Make FLAC (embed metadata and location picture/map)
- Make Opus
- Upload to IA

## Bext Coding History Example
A=ANALOGUE,M=stereo,T=Sony TC-D5 PROII; 1 7/8 ips; Compact Cassette

A=PCM,F=96000,W=24,M=stereo,T=Zoom; UAC-2; SN006082, A/D

## Location metadata
'LOCATION'  ISO 6709 (to five decimals, minus trailing slash) Example: +40.81013-073.94758

## FLAC embed metadata example commands
`metaflac --import-picture-from="13||||/Users/weevz/Desktop/HarlemRain.jpg" /Users/weevz/Desktop/HarlemRain.flac`

`--set-tag=SOURCEMEDIA="A=ANALOGUE,M=stereo,T=Sony TC-D5 PROII; 1 7/8 ips; Compact Cassette" --set-tag=LOCATION="+40.81013-073.94758" --set-tag=DATE="2017-03-18 (recorded)" --set-tag=LICENSE="CC BY 4.0" --import-picture-from="13||||/Users/weevz/Desktop/HarlemRain.jpg"`
