[![][logo]](http://www.emr.ai)
# Synthetic Diarization Corpus


[logo]: http://emr.ai/wp-content/uploads/2017/05/emr.ai_LOGO.png?x92422

## Introduction

A synthetic corpus of dialogs was constructed from the LibriSpeech corpus,
and is made freely available for diarization research. It includes over 90 hours
of training data, and over 9 hours each of development and test data. 
Both 2-person and 3-person dialogs, with and without overlap, are included. 
Timing information is provided in several formats, and includes not only speaker segmentations, 
but also phoneme segmentations. As such, it is a useful starting point for general, 
particularly early-stage, diarization system development.

## How to use

The corpus contains 4 top-level directories:

<br>librispeech2: 2-person dialogs
<br>librispeech2o: 2-person dialogs with overlap
<br>librispeech3: 3-person dialogs
<br>librispeech3o: 3-person dialogs with overlap

<br>All sub-directories are "Kaldi table" data directories.
Audio files are 16kHz PCM 16bit little-endian mono encoded.

### Formats

<br>ctm - each line is <F> <C> <BT> <DUR> word
<br>    Where:
<br>        <F> The waveform filename. NOTE: no pathnames or extensions are expected. 
<br>        <C> Speaker.
<br>        <BT> The begin time (seconds) of the segment, measured from the start time of the file. 
<br>        <DUR> The duration (seconds) of the segment.
<br>labs - each line is a speaker id or 0 for pauses. One line corresponds 0.01 seconds of audio.
<br>rttm0 - Rich Transcription Time Marked file format. Full specification can be found in Appendix A of "NIST's The 2009 (RT-09) Rich Transcription Meeting Recognition Evaluation Plan" paper.
<br>rttm - merged rttm0, without pauses

This corpus is licensed under [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/), but requires the following reference:
> Erik Edwards, Michael Brenndoerfer, David Suendermann, XXXXX 2018 (submitted)

#### Bibtex
``` 
@article{Edwards18_SynDiaCorpus,
	Author = {Edwards, E and Brenndoerfer, M and Suendermann, D},
	Title = {TITLE: XXX},
	Year = {2018} 
}
```   



Based on the [LibriSpeech ASR corpus](http://www.openslr.org/12/ "OpenSLR")

