# Summary

The Spoken Slovenian Treebank (SST) is a manually annotated collection of transcribed audio recordings featuring spontaneous speech in various everyday situations. It includes 344 unique speech events (documents) amounting to approximately 10 hours of speech, encompassing a total of 6,107 utterances and 98,396 tokens.

# Introduction

Spoken Slovenian Treebank (SST) is a manually grammatically annotated sample of the [GOS reference corpus](http://hdl.handle.net/11356/1863) of spoken Slovenian. It contains transcribed audio recordings of monologic, dialogic and multi-pary spontaneous speech in different everyday situations, balanced so as to be representative of speaker demographics (sex, age, region, education), channels (TV, radio, telephone, personal contact) and communication settings (TV and radio shows, lectures, meetings, consultations, services, conversations between friends etc.).

The spelling, tokenization and segmentation principles follow the transcription guidelines of the reference corpus (Verdonik et al. 2013) with the syntactic trees spanning over individual utterances (semantically, syntactically and acoustically delimited units, roughly corresponding to written-like sentences). The annotation has been performed on top of normalized transcriptions, i.e. words with standardized spelling. To accommodate the structural and pragmatic particularities of spoken language data, such as self-repairs, fillers, discourse markers and parentheticals, we relied on the guidelines proposed by Dobrovoljc and Nivre (2016) and Dobrovoljc (2022).

As of UD release v2.14 in May 2024, the original version of the SST UD treebank (Dobrovoljc in Nivre 2016) has been partially revised and substantially extended with new data from GOS v2 (Verdonik et al. 2024), such as parliamentary debates, round tables and online events. The latest version of the SST treebank thus includes 6,107 utterances, produced by 676 speakers in 344 different speech events (48% public and 52% non-public tokens) amounting to approximately 10 hours of recordings. For the UD release v2.15 (November 2025), punctuation symbols such as commas and sentence-final punctuation, which were previously missing, have been added.

The train-dev-test data split has been randomized on document-level. The CONLL-U files include links to original audio recordings, and information on the GOS speaker/event IDs, which can be used to retrieve additional metadata information from the original GOS corpus, such as the information on speaker demographics, speech event details or transcribed markers of prosody.

## Acknowledgments

We wish to thank all the collaborators who have helped with dependency annotation (Nives Hüll, Karolina Zgaga, Luka Terčon, Matija Škofljanec), JOS-MTE lemmatization and morphological annotation (Jaka Čibej, Tina Munda, Matija Škofljanec), punctuation insertion (Iztok Lebar Bajec, Tina Munda), data sampling (Darinka Verdonik, Nikola Ljubešić, Peter Rupnik), automatic pre-annotation (Luka Krsnik), JOS-to-UD morphology conversion (Jaka Čibej), and guidelines consulting (Joakim Nivre). This work was financially supported by the Slovenian Research and Innovation Agency (grant no. Z6-4617 - [A Treebank-Driven Approach to the Study of Spoken Slovenian](https://spot.ff.uni-lj.si/en/) and Young Researcher Programme 2013) and IC1207 COST Action PARSEME.


## References
* Kaja Dobrovoljc and Joakim Nivre. 2016. The Universal Dependencies Treebank of Spoken Slovenian. In: Proceedings of the Tenth International Conference on Language Resources and Evaluation (LREC’16), Portorož, Slovenia.

```
@inproceedings{dobrovoljc-nivre-2016-universal,
    title = "The {U}niversal {D}ependencies Treebank of Spoken {S}lovenian",
    author = "Dobrovoljc, Kaja and Nivre, Joakim",
    booktitle = "Proceedings of the Tenth International Conference on Language Resources and Evaluation ({LREC}'16)",
    year = "2016",
    publisher = "European Language Resources Association (ELRA)",
    url = "https://aclanthology.org/L16-1248",
    pages = "1566--1573",
}
```

### Other references
* Verdonik et al. 2013. Compilation, transcription and usage of a reference speech corpus: the case of the Slovene corpus GOS. Language Resources and  Evaluation, 47(4):1031–1048.
* Verdonik et al. 2024. Gos 2: A New Reference Corpus of Spoken Slovenian. LREC-COLING 2024.
* Kaja Dobrovoljc. 2022. [Spoken Language Treebanks in Universal Dependencies: An Overview](https://aclanthology.org/2022.lrec-1.191/). LREC 2022.


## Changelog
<pre>
2024-07-15 v2.15
    * Added punctuation symbols (22,055 new tokens)
    * Corrected some errors in manual transcription and annotation
    * Updated readme   

2024-04-11 v2.14
    * Extended original dataset with 2,916 new sentences (46,853 tokens)
    * Revised original dataset to implement guidelines changes (e.g. reparandum and discourse)
    * Removed conj:extend label
    * Added Gos2.1 document/sentence/token IDs for easier lookup
    * Changed license to CC-BY-SA
    * Updated readme   


2023-04-12 v2.12
    * Added metadata information on speaker ID and soundfile URL
    * Renamed sentence IDs to comply with the GOS 2.0 nomenclature
    * Corrected mistakes pertaining to Reflex and Polarity features
    * Corrected inconsistent UPOS tags for non-lexical tokens (all PUNCT)
    * Corrected some minor errors in manual annotation
    * Removed old msd info from MISC and renamed 'word' to 'pronunciation'

2022-04-20 v2.10
    * Manual relabelling of the few examples raising validation errors, mostly from goeswith to fixed

2019-10-30 v2.5
    * Fixed legacy validation errors, i.e.
      * Re-tagging the [gap]-like punctuation from X to PUNCT
      * Re-attaching the [gap]-like punctuation causing non-projectivity
      * Re-attaching leafs of unlike parents
      * Fixing random mistakes in annotation

2015-01-30 v2.0
    * Manual and automatic conversions from UDv1 to UDv2 guidelines
    * Manual corrections of some mistakes in previous versions
    * Resizing of train-dev-test (in accordance with CONLL ST 2017 requirements)
    * Random utterance shuffling to ensure more representative genre distributions.
    
2015-03-15 v2.2
    * Manual corrections of some mistakes in previous versions
    * New (text-level) data randomization
    * Resizing of train-test datasets (in accordance with CONLL ST 2018)
</pre>

<pre>
=== Machine-readable metadata (DO NOT REMOVE!) ================================
Data available since: UD v1.3
License: CC BY-SA 4.0
Includes text: yes
Genre: spoken
Lemmas: converted from manual
UPOS: converted from manual
XPOS: manual native
Features: converted from manual
Relations: manual native
Contributors: Dobrovoljc, Kaja; Nivre, Joakim
Contributing: elsewhere
Contact: kaja.dobrovoljc@ff.uni-lj.si
===============================================================================
</pre>
