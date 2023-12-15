---
language: fr
license: mit
multilinguality: monolingual
task_categories:
  - automatic-speech-recognition
  - voice-activity-detection
---
# Simsamu dataset

This repository contains recordings of simulated medical dispatch dialogs in the
french language, annotated for diarization and transcription. It is published
under the MIT license.

These dialogs were recorded as part of the training of emergency medicine
interns, which consisted in simulating a medical dispatch call where the interns
took turns playing the caller and the regulating doctor. 

Each situation was decided randomly in advance, blind to who was playing the
medical dispatcher (e.g., road accident, chest pain, burns, etc.).  The
affiliations between the caller and the patient  (family, friend, colleague...)
and the caller's communication mode is then randomly selected. The caller had to
adapt his or her performance to the communication mode associated with the
situation. Seven communication modes were defined: shy, procedural, angry,
cooperative, frightened, impassive, incomprehensible. 

Regarding sound quality, the voice of the regulating doctor is directly picked
up by a microphone, whereas the voice of the caller is transmitted through the
phone network and re-emitted by a phone speaker before being picked up by the
microphone. This leads to different acoustic characteristics between the
caller's voice and the regulator's, the later one often being much clearer. This
phenomena is also present in actual dispatch services recordings, where the
regulator's voice is directly recorded in a quiet room whereas the caller is
often calling from noisier environments and its voice is altered by the phone
network compression.

The dataset is composed of 61 audio recordings with a total duration of 3h 15
and an average duration per recording of 3 minutes 11 seconds. Each recording is
available as a `.m4a` audio file with 8KHz sample rate and a 128 Kbps bitrate.
The diarization data is available in a corresponding `.rttm` file and the
transcription in an `.srt` file.

An additional `metadata.csv` contains speaker ids for callers and regulators in
each recording.

See also: [Simsamu diarization
pipeline](https://huggingface.co/medkit/simsamu-diarization)

See also: [Simsamu transcription
model](https://huggingface.co/medkit/simsamu-transcription)
