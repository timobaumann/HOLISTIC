# The HOLISTIC challenge at Interspeech 2019

We are excited to invite participants to the **"How far is the end-of-utterance"** challenge!

The naming of the HOLISTIC challenge is a tribute to the seminal paper **“How long is the sentence?”** (Grosjean, 1983). 
The Swiss psycholinguist used gating experiments to show that listeners are capable to estimate the duration 
remaining of a sentence from its initial (gated) part without the help of sentential priors. 
He proposed that the information is in the prosody of the gated signal. 
These experimental results have been assessed by other methods such as button-press or brain responses.
A second derivation of the challenge name is the fact that determining the end of a contribution in speech grounds in many fields of linguistics, from prosody to syntax and semantics. It is for this reason that we find our challenge to be a particularly good match for 

**What about machines?** Prediction of End-of-Utterance (EoU), Sentence (EoS) and Turn (EoT) is an important component of natural speech and language processing for interactive systems, and in particular for incremental systems that shall initiate action even before an utterance is finished (e.g., start moving the head of a robot).
It is a prerequisite for timely backchanneling or turn taking. Several systems have already been proposed for incremental dialog systems. For some tasks, particularly embodied robotic systems, the \emph{anticipation} of the end of utterance, rather than quick reaction to it, is particularly relevant.

The HOLISTIC challenge aims at gathering speech scientists and technologists around a common analysis and test bed, where analysis of performance of various predictive models on large data sets can be shared.

## Tasks
The task of the challenge is to incrementally estimate how much material is sill missing until 
the end of the user utterance (EoU) based on the audio that has been produced (and perceived) so far.
The aim is thus to go beyond a simple incremental Voice Activity Detector (VAD); each speech frame is complemented with its discretized distance to the EoU [6-valued cue]: 1) >500 ms; 2) [500-400[ ms; 3) [400-300[ ms; 4) [300-200[ ms; 5) [200-100[; 6) <100ms

The tasks consist in associating each 10ms signal frame with one out of 7 labels: 0 for silent frames, [1-6] for speech frames accprding to their relative distance from upcoming EoU.

## Data
In this first challenge, we focus on read speech. We will extend the task to dialogic, 
multimodal and/or multiparty conversation data in future iterations of the challenge.

We deliver data from the **Spoken Wikipedia Corpus** in several languages (German, English, French) that has been automatically parsed by a robust VAD. We provide raw signals sampled at 16khz together with .TextGrid files segmented into alternating silent intervals (labelled as **"__"**) and speech intervals (labelled as **"utt"**).

1. American-English data: 1000 hours [.tar]
2. German data: xx hours [.tar]
3. French data: 10 hours [[Wikimedia_FR.tar.gz; 148 articles; 4.8Go|https://drive.google.com/file/d/19RjZfzt5oPOWlOQXJRG36-TKpxSG-IG8/view?usp=sharing]]

## Tracks
You can compete in two tracks:
1. Signal-based EoU estimation. These end-to-end predictors should be language-independent and consider speech frames as input.
2. Language-specific EoU estimation. These predictors may exploit incremental ASR results that reflect what a system 
would be able to perceive at the given point in time in the middle of an utterance.

## Dissemination of the results
The results will be disseminated through the HOLISTIC Special Session at Interspeech 2019 (our special session proposal was accepted). Besides prediction scores, we ask each participant to send their system descriptions (but not codes/scripts) - similar to the NIST SREs. We will submit a challenge summary paper to Interspeech, and  encourage the participants to submit papers describing their individual systems. This way the accepted papers would be available through the ISCA Archive in the Interspeech proceedings.

## Organizers

> **Timo Baumann**, Language Technologies Institute, Carnegie Mellon University, Pittsburg - USA

Dr. Baumann is a systems scientist at LTI/CMU with expertise in speech and 
prosody processing and is a leader in incremental processing for interactive systems. 
He has lead the Spoken Wikipedia Corpus collection project, which collected more than 
1000 hours of read speech from Wikipedia and produced corresponding alignments. 

> **Gérard Bailly**, GIPSA-lab, Grenoble-Alpes University, Grenoble - France

Prof. Bailly is a senior CNRS researcher at GIPSA-lab and
a specialist of speech communication. He was deputy director of the lab (2008-12). He supervised 28 PhD theses, authored 44 journal articles and 250 papers in major international conferencess and coedited “Talking Machines: Theories, Models \& Designs” (1992), “Improvements in Speech Synthesis” (2002) and “Audiovisual speech processing” (2012). His current interest is multimodal interaction with conversational agents (including the humanoid robot iCub).
