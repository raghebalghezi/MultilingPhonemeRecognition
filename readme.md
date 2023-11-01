# Multilingual Phoneme Recognition

## Project

Carefully read the section related to the Project on MyCourses: https://mycourses.aalto.fi/mod/page/view.php?id=1095126. I advise you to start the writing process now. Please set up an Overleaf document and share it with me. I will provide feedback directly on Overleaf. Everytime you make progress, you can submit it 


## What?
A phoneme recognizer is an automatic speech recognition system (ASR) that converts speech into a sequence of phonemes. A phoneme is the smallest phonological unit of speech. To see it in action, check the demo at: https://huggingface.co/facebook/wav2vec2-lv-60-espeak-cv-ft . If the demo does not work, try the code version in Google Colab.

## Purpose:
Imagine you are trying to develop an app that helps students learn/practice pronunciation skills in a foreign language. A phoneme recognizer can diagnose the student's pronunciation and provide them with immediate feedback, which is important for language learning purposes. A multilingual phoneme recognizer allows us to develop one system for multiple languages. Imagine you want to develop an app for three languages: Finnish, Swedish, and Norwegian. Developing three separate recognizers is not only computationally intensive, but it is also labor- intensive.

## Assignment:
For this week, I would like you to read the paper below. Do not worry if you don't understand everything. The point is to familiarize yourself with the topic. Most importantly, check the demo above and try to run and play with it so you understand what a phoneme recognizer is and what it does.

## Data

1. https://huggingface.co/blog/fine-tune-xlsr-wav2vec2 
2. https://huggingface.co/datasets/facebook/voxpopuli/viewer/fi
3. https://huggingface.co/datasets/Sprakbanken/nb_samtale 

## Baseline

Each team member should go through the tutorial (https://huggingface.co/blog/fine-tune-xlsr-wav2vec2) using one dataset from data section. First, we would like to know the models' inherent performance without training, so we can use (xlsr-wav2vec2 and wav2vec2-lv-60-espeak-cv-ft) off-the-shelf on the test set of the Voxpopuli-FI and nb_samtale datasets. This is going to serve as a baseline to our experiments. Next, we will divide the work among the three team members such that each member takes care of one dataset. 


## Goal

The overall goal is to answer the research question: how well does the phoneme recognizer perform compared to ASR in terms of CER/PER? Does training on one language lead to performance in another? e.g. if we train on Finnish, does it the performace on Norwegian improves and vise versa? etc.

## Exps

1. test the performance of xlsr-wav2vec2 on the test set of Voxpopuli-FI and nb_samtale.
2. Finetune xlsr-wav2vec2 on the validation sets of Voxpopuli-FI and nb_samtale and compare the performance.
3. test the performance of wav2vec2-lv-60-espeak-cv-ft on the test set of Voxpopuli-FI and nb_samtale.
4. Finetune wav2vec2-lv-60-espeak-cv-ft on the validation sets of Voxpopuli-FI and nb_samtale and compare the performance.
5. Finetune wav2vec2-lv-60-espeak-cv-ft on the validation set of Voxpopuli-FI and test on nb_samtale and vice versa. Compare the performance.

NOTE: because wav2vec2-lv-60-espeak-cv-ft is a phoneme recognizer, the transcript labels needs to be converted to IPA phoneme sequences. Use https://bootphon.github.io/phonemizer/python_examples.html to convert text to IPA. 





## Reference:
1. Simple and Effective Zero-shot Cross-lingual Phoneme Recognition: https://arxiv.org/abs/2109.11680"
2. Universal Phone Recognition with a Multilingual Allophone System: https://arxiv.org/abs/2002.11800
