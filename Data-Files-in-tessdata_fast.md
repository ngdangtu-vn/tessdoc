## Traineddata Files for Version 4.00 

We have three sets of .traineddata files for tesseract on GitHub in three separate repositories. 

* [tessdata_fast](https://github.com/tesseract-ocr/tessdata_fast) (Sep 2017) best "value for money" in speed vs accuracy, Integer models
* [tessdata_best](https://github.com/tesseract-ocr/tessdata_best) (Sep 2017) best results on the eval data, slower, Float models, can be used as base for finetune training
* [tessdata](https://github.com/tesseract-ocr/tessdata) (Nov 2016) supports legacy tesseract engine also

When using the models in the **`tessdata_best`** and **`tessdata_fast`** repositories, only the new LSTM-based OCR engine is supported. The legacy tesseract engine is NOT supported with these files, so Tesseract's oem modes '0' and '2' won't work with them. 

## Information specific to tessdata_fast

First, fast is trained with a spec that produces a smaller net than best. As a result of smaller model, the prediction will be faster.
Then, the float->int conversion is done, which further reduces the size of the model and makes it even faster if your CPU supports AVX2.

### Usage

Most users will use **`tessdata_fast`** for OCR as that is what will be shipped as part of Debian and Ubuntu distributions and will provide accurate and fast recognition. 

### Version string : 4.00.00alpha : [Network specification]

```

Version string:4.00.00alpha:afr:synth20170629:[1,36,0,1Ct3,3,16Mp3,3Lfys64Lfx96Lrx96Lfx512O1c1]
LSTM training info:Network str:[1,36,0,1Ct3,3,16Mp3,3Lfys64Lfx96Lrx96Lfx512O1c1], flags=41, iteration=286700, sample_iteration=286724, null_char=95, learning_rate=0.001, momentum=0.5, adam_beta=0.999

Version string:4.00.00alpha:amh:synth20170629
LSTM training info:Network str:[1,36,0,1Ct3,3,16Mp3,3Lfys48Lfx96Lrx96Lfx192O1c1], flags=41, iteration=6112200, sample_iteration=6112270, null_char=284, learning_rate=0.001, momentum=0.5, adam_beta=0.999

Version string:4.00.00alpha:Arabic:synth20170629:[1,48,0,1Ct3,3,16Mp3,3Lfys64Lfx96Lrx96Lfx128O1c1]
LSTM training info:Network str:[1,48,0,1Ct3,3,16Mp3,3Lfys64Lfx96Lrx96Lfx128O1c1], flags=41, iteration=5524000, sample_iteration=5532770, null_char=2, learning_rate=0.001, momentum=0.5, adam_beta=0.999

Version string:4.00.00alpha:ara:synth20170629
LSTM training info:Network str:[1,48,0,1Ct3,3,16Mp3,3Lfys64Lfx96Lrx96Lfx192O1c1], flags=41, iteration=5521100, sample_iteration=5544718, null_char=2, learning_rate=0.001, momentum=0.5, adam_beta=0.999

Version string:4.00.00alpha:Armenian:synth20170629:[1,36,0,1Ct3,3,16Mp3,3Lfys64Lfx96Lrx96Lfx384O1c1]
LSTM training info:Network str:[1,36,0,1Ct3,3,16Mp3,3Lfys64Lfx96Lrx96Lfx384O1c1], flags=41, iteration=2036600, sample_iteration=2037181, null_char=191, learning_rate=0.001, momentum=0.5, adam_beta=0.999

Version string:4.00.00alpha:asm:synth20170629
LSTM training info:Network str:[1,48,0,1Ct3,3,16Mp3,3Lfys64Lfx64Lrx64Lfx512O1c1], flags=41, iteration=2758500, sample_iteration=2758570, null_char=2, learning_rate=0.001, momentum=0.5, adam_beta=0.999

Version string:4.00.00alpha:aze_cyrl:synth20170629
LSTM training info:Network str:[1,36,0,1Ct3,3,16Mp3,3Lfys64Lfx96Lrx96Lfx192O1c1], flags=41, iteration=7665300, sample_iteration=7666563, null_char=88, learning_rate=0.001, momentum=0.5, adam_beta=0.999

Version string:4.00.00alpha:aze:synth20170629
LSTM training info:Network str:[1,36,0,1Ct3,3,16Mp3,3Lfys64Lfx96Lrx96Lfx192O1c1], flags=41, iteration=6760000, sample_iteration=6760858, null_char=88, learning_rate=0.001, momentum=0.5, adam_beta=0.999

Version string:4.00.00alpha:bel:synth20170629:[1,36,0,1Ct3,3,16Mp3,3Lfys48Lfx96Lrx96Lfx128O1c1]
LSTM training info:Network str:[1,36,0,1Ct3,3,16Mp3,3Lfys48Lfx96Lrx96Lfx128O1c1], flags=41, iteration=3105300, sample_iteration=3105747, null_char=95, learning_rate=0.001, momentum=0.5, adam_beta=0.999

Version string:4.00.00alpha:Bengali:synth20170629:[1,48,0,1Ct3,3,16Mp3,3Lfys64Lfx96Lrx96Lfx384O1c1]
LSTM training info:Network str:[1,48,0,1Ct3,3,16Mp3,3Lfys64Lfx96Lrx96Lfx384O1c1], flags=41, iteration=1111400, sample_iteration=1111452, null_char=2, learning_rate=0.001, momentum=0.5, adam_beta=0.999

Version string:4.00.00alpha:ben:synth20170629
LSTM training info:Network str:[1,36,0,1Ct3,3,16Mp3,3Lfys64Lfx96Lrx96Lfx192O1c1], flags=41, iteration=807100, sample_iteration=807306, null_char=2, learning_rate=0.001, momentum=0.5, adam_beta=0.999

Version string:4.00.00alpha:bod:synth20170629
LSTM training info:Network str:[1,48,0,1Ct3,3,16Mp3,3Lfys64Lfx96Lrx96Lfx384O1c1], flags=41, iteration=3513900, sample_iteration=3524222, null_char=2, learning_rate=0.001, momentum=0.5, adam_beta=0.999

Version string:4.00.00alpha:bos:synth20170629
LSTM training info:Network str:[1,48,0,1Ct3,3,16Mp3,3Lfys64Lfx96Lrx96Lfx192O1c1], flags=41, iteration=3258400, sample_iteration=3258771, null_char=95, learning_rate=0.001, momentum=0.5, adam_beta=0.999

Version string:4.00.00alpha:bre:synth20170629
LSTM training info:Network str:[1,48,0,1Ct3,3,16Mp3,3Lfys64Lfx64Lrx64Lfx512O1c1], flags=41, iteration=14000, sample_iteration=14000, null_char=124, learning_rate=0.001, momentum=0.5, adam_beta=0.999

Version string:4.00.00alpha:bul:synth20170629:[1,36,0,1Ct3,3,16Mp3,3Lfys48Lfx96Lrx96Lfx128O1c1]
LSTM training info:Network str:[1,36,0,1Ct3,3,16Mp3,3Lfys48Lfx96Lrx96Lfx128O1c1], flags=41, iteration=1801400, sample_iteration=1802032, null_char=92, learning_rate=0.001, momentum=0.5, adam_beta=0.999

Version string:4.00.00alpha:Canadian_Aboriginal:synth20170629
LSTM training info:Network str:[1,48,0,1Ct3,3,16Mp3,3Lfys64Lfx96Lrx96Lfx384O1c1], flags=41, iteration=1949300, sample_iteration=1949421, null_char=652, learning_rate=0.001, momentum=0.5, adam_beta=0.999

Version string:4.00.00alpha:cat:synth20170629:[1,36,0,1Ct3,3,16Mp3,3Lfys48Lfx96Lrx96Lfx192O1c1]
LSTM training info:Network str:[1,36,0,1Ct3,3,16Mp3,3Lfys48Lfx96Lrx96Lfx192O1c1], flags=41, iteration=2427200, sample_iteration=2427351, null_char=88, learning_rate=0.001, momentum=0.5, adam_beta=0.999

Version string:4.00.00alpha:ceb:synth20170629
LSTM training info:Network str:[1,36,0,1Ct3,3,16Mp3,3Lfys64Lfx96Lrx96Lfx192O1c1], flags=41, iteration=6718000, sample_iteration=6772655, null_char=73, learning_rate=0.001, momentum=0.5, adam_beta=0.999

Version string:4.00.00alpha:ces:synth20170629:[1,36,0,1Ct3,3,16Mp3,3Lfys64Lfx96Lrx96Lfx192O1c1]
LSTM training info:Network str:[1,36,0,1Ct3,3,16Mp3,3Lfys64Lfx96Lrx96Lfx192O1c1], flags=41, iteration=2058000, sample_iteration=2058141, null_char=121, learning_rate=0.001, momentum=0.5, adam_beta=0.999

Version string:4.00.00alpha:Cherokee:synth20170629
LSTM training info:Network str:[1,36,0,1Ct3,3,16Mp3,3Lfys64Lfx96Lrx96Lfx192O1c1], flags=41, iteration=7542100, sample_iteration=7542435, null_char=191, learning_rate=0.001, momentum=0.5, adam_beta=0.999

Version string:4.00.00alpha:chi_sim:synth20170629:[1,48,0,1Ct3,3,16Mp3,3Lfys64Lfx96Lrx96Lfx512O1c1]
LSTM training info:Network str:[1,48,0,1Ct3,3,16Mp3,3Lfys64Lfx96Lrx96Lfx512O1c1], flags=41, iteration=1971300, sample_iteration=1976813, null_char=223, learning_rate=0.001, momentum=0.5, adam_beta=0.999

Version string:4.00.00alpha:chi_sim_vert:synth20170629
LSTM training info:Network str:[1,36,0,1Ct3,3,16Mp3,3Lfys64Lfx96Lrx96Lfx384O1c1], flags=41, iteration=3656700, sample_iteration=3679197, null_char=223, learning_rate=0.001, momentum=0.5, adam_beta=0.999

Version string:4.00.00alpha:chi_tra:synth20170629:[1,48,0,1Ct3,3,16Mp3,3Lfys64Lfx96Lrx96Lfx512O1c1]
LSTM training info:Network str:[1,48,0,1Ct3,3,16Mp3,3Lfys64Lfx96Lrx96Lfx512O1c1], flags=41, iteration=1988000, sample_iteration=1992889, null_char=226, learning_rate=0.001, momentum=0.5, adam_beta=0.999

Version string:4.00.00alpha:chi_tra_vert:synth20170629
LSTM training info:Network str:[1,36,0,1Ct3,3,16Mp3,3Lfys64Lfx96Lrx96Lfx384O1c1], flags=41, iteration=3846900, sample_iteration=3902087, null_char=226, learning_rate=0.001, momentum=0.5, adam_beta=0.999

Version string:4.00.00alpha:chr:synth20170629
LSTM training info:Network str:[1,36,0,1Ct3,3,16Mp3,3Lfys48Lfx96Lrx96Lfx128O1c1], flags=41, iteration=7847200, sample_iteration=7847486, null_char=102, learning_rate=0.001, momentum=0.5, adam_beta=0.999

Version string:4.00.00alpha:cos:synth20170629
LSTM training info:Network str:[1,36,0,1Ct3,3,16Mp3,3Lfys64Lfx96Lrx96Lfx384O1c1], flags=41, iteration=5120400, sample_iteration=5120693, null_char=104, learning_rate=0.001, momentum=0.5, adam_beta=0.999

Version string:4.00.00alpha:cym:synth20170629
LSTM training info:Network str:[1,36,0,1Ct3,3,16Mp3,3Lfys64Lfx96Lrx96Lfx384O1c1], flags=41, iteration=4212000, sample_iteration=4212285, null_char=108, learning_rate=0.001, momentum=0.5, adam_beta=0.999

Version string:4.00.00alpha:Cyrillic:synth20170629
LSTM training info:Network str:[1,36,0,1Ct3,3,16Mp3,3Lfys64Lfx96Lrx96Lfx128O1c1], flags=41, iteration=3401300, sample_iteration=3402083, null_char=202, learning_rate=0.001, momentum=0.5, adam_beta=0.999

Version string:4.00.00alpha:dan:synth20170629
LSTM training info:Network str:[1,48,0,1Ct3,3,16Mp3,3Lfys64Lfx96Lrx96Lfx128O1c1], flags=41, iteration=4983400, sample_iteration=4983829, null_char=100, learning_rate=0.001, momentum=0.5, adam_beta=0.999

Version string:4.00.00alpha:deu:synth20170629:[1,36,0,1Ct3,3,16Mp3,3Lfys64Lfx96Lrx96Lfx192O1c1]
LSTM training info:Network str:[1,36,0,1Ct3,3,16Mp3,3Lfys64Lfx96Lrx96Lfx192O1c1], flags=41, iteration=4860000, sample_iteration=4860533, null_char=114, learning_rate=0.001, momentum=0.5, adam_beta=0.999

Version string:4.00.00alpha:Devanagari:synth20170629
LSTM training info:Network str:[1,36,0,1Ct3,3,16Mp3,3Lfys48Lfx96Lrx96Lfx192O1c1], flags=41, iteration=5059200, sample_iteration=5060646, null_char=2, learning_rate=0.001, momentum=0.5, adam_beta=0.999

Version string:4.00.00alpha:div:synth20170629
LSTM training info:Network str:[1,48,0,1Ct3,3,16Mp3,3Lfys64Lfx96Lrx96Lfx192O1c1], flags=41, iteration=3249400, sample_iteration=3256730, null_char=2, learning_rate=0.001, momentum=0.5, adam_beta=0.999

Version string:4.00.00alpha:dzo:synth20170629
LSTM training info:Network str:[1,48,0,1Ct3,3,16Mp3,3Lfys64Lfx96Lrx96Lfx192O1c1], flags=41, iteration=4258800, sample_iteration=4335799, null_char=2, learning_rate=0.001, momentum=0.5, adam_beta=0.999

Version string:4.00.00alpha:ell:synth20170629:[1,36,0,1Ct3,3,16Mp3,3Lfys48Lfx96Lrx96Lfx128O1c1]
LSTM training info:Network str:[1,36,0,1Ct3,3,16Mp3,3Lfys48Lfx96Lrx96Lfx128O1c1], flags=41, iteration=3725500, sample_iteration=3725577, null_char=213, learning_rate=0.001, momentum=0.5, adam_beta=0.999

Version string:4.00.00alpha:eng:synth20170629
LSTM training info:Network str:[1,36,0,1Ct3,3,16Mp3,3Lfys48Lfx96Lrx96Lfx192O1c1], flags=41, iteration=6352400, sample_iteration=6352704, null_char=110, learning_rate=0.001, momentum=0.5, adam_beta=0.999

Version string:4.00.00alpha:enm:synth20170629
LSTM training info:Network str:[1,36,0,1Ct3,3,16Mp3,3Lfys64Lfx96Lrx96Lfx512O1c1], flags=41, iteration=2720200, sample_iteration=2721910, null_char=104, learning_rate=0.001, momentum=0.5, adam_beta=0.999

Version string:4.00.00alpha:epo:synth20170629
LSTM training info:Network str:[1,36,0,1Ct3,3,16Mp3,3Lfys48Lfx96Lrx96Lfx192O1c1], flags=41, iteration=6842600, sample_iteration=6843069, null_char=101, learning_rate=0.001, momentum=0.5, adam_beta=0.999

Version string:4.00.00alpha:est:synth20170629
LSTM training info:Network str:[1,36,0,1Ct3,3,16Mp3,3Lfys48Lfx96Lrx96Lfx128O1c1], flags=41, iteration=7906300, sample_iteration=7907020, null_char=103, learning_rate=0.001, momentum=0.5, adam_beta=0.999

Version string:4.00.00alpha:Ethiopic:synth20170629
LSTM training info:Network str:[1,36,0,1Ct3,3,16Mp3,3Lfys48Lfx96Lrx96Lfx128O1c1], flags=41, iteration=149100, sample_iteration=149101, null_char=385, learning_rate=0.001, momentum=0.5, adam_beta=0.999

Version string:4.00.00alpha:eus:synth20170629
LSTM training info:Network str:[1,36,0,1Ct3,3,16Mp3,3Lfys64Lfx96Lrx96Lfx192O1c1], flags=41, iteration=15200, sample_iteration=15204, null_char=89, learning_rate=0.001, momentum=0.5, adam_beta=0.999

Version string:4.00.00alpha:fao:synth20170629
LSTM training info:Network str:[1,48,0,1Ct3,3,16Mp3,3Lfys64Lfx96Lrx96Lfx384O1c1], flags=41, iteration=2812800, sample_iteration=2812950, null_char=126, learning_rate=0.001, momentum=0.5, adam_beta=0.999

Version string:4.00.00alpha:fas:synth20170629:[1,36,0,1Ct3,3,16Mp3,3Lfys48Lfx96Lrx96Lfx128O1c1]
LSTM training info:Network str:[1,36,0,1Ct3,3,16Mp3,3Lfys48Lfx96Lrx96Lfx128O1c1], flags=41, iteration=2762200, sample_iteration=2773866, null_char=2, learning_rate=0.001, momentum=0.5, adam_beta=0.999

Version string:4.00.00alpha:fil:synth20170629
LSTM training info:Network str:[1,36,0,1Ct3,3,16Mp3,3Lfys48Lfx96Lrx96Lfx128O1c1], flags=41, iteration=7435100, sample_iteration=7435587, null_char=81, learning_rate=0.001, momentum=0.5, adam_beta=0.999

Version string:4.00.00alpha:fin:synth20170629
LSTM training info:Network str:[1,36,0,1Ct3,3,16Mp3,3Lfys64Lfx96Lrx96Lfx384O1c1], flags=41, iteration=3741900, sample_iteration=3742321, null_char=94, learning_rate=0.001, momentum=0.5, adam_beta=0.999

Version string:4.00.00alpha:Fraktur:synth20170629
LSTM training info:Network str:[1,48,0,1Ct3,3,16Mp3,3Lfys64Lfx96Lrx96Lfx384O1c1], flags=41, iteration=3739900, sample_iteration=3740440, null_char=166, learning_rate=0.001, momentum=0.5, adam_beta=0.999

Version string:4.00.00alpha:fra:synth20170629:[1,36,0,1Ct3,3,16Mp3,3Lfys48Lfx96Lrx96Lfx128O1c1]
LSTM training info:Network str:[1,36,0,1Ct3,3,16Mp3,3Lfys48Lfx96Lrx96Lfx128O1c1], flags=41, iteration=2330100, sample_iteration=2330256, null_char=139, learning_rate=0.001, momentum=0.5, adam_beta=0.999

Version string:4.00.00alpha:frk:synth20170629
LSTM training info:Network str:[1,48,0,1Ct3,3,16Mp3,3Lfys64Lfx96Lrx96Lfx384O1c1], flags=41, iteration=3692700, sample_iteration=3692967, null_char=98, learning_rate=0.001, momentum=0.5, adam_beta=0.999

Version string:4.00.00alpha:frm:synth20170629
LSTM training info:Network str:[1,48,0,1Ct3,3,16Mp3,3Lfys64Lfx96Lrx96Lfx128O1c1], flags=41, iteration=176600, sample_iteration=176697, null_char=140, learning_rate=0.001, momentum=0.5, adam_beta=0.999

Version string:4.00.00alpha:fry:synth20170629
LSTM training info:Network str:[1,48,0,1Ct3,3,16Mp3,3Lfys64Lfx96Lrx96Lfx384O1c1], flags=41, iteration=3246500, sample_iteration=3246617, null_char=106, learning_rate=0.001, momentum=0.5, adam_beta=0.999

Version string:4.00.00alpha:Georgian:synth20170629
LSTM training info:Network str:[1,48,0,1Ct3,3,16Mp3,3Lfys64Lfx96Lrx96Lfx384O1c1], flags=41, iteration=2308600, sample_iteration=2310386, null_char=225, learning_rate=0.001, momentum=0.5, adam_beta=0.999

Version string:4.00.00alpha:gla:synth20170629
LSTM training info:Network str:[1,48,0,1Ct3,3,16Mp3,3Lfys64Lfx96Lrx96Lfx384O1c1], flags=41, iteration=3365500, sample_iteration=3365659, null_char=104, learning_rate=0.001, momentum=0.5, adam_beta=0.999

Version string:4.00.00alpha:gle:synth20170629
LSTM training info:Network str:[1,48,0,1Ct3,3,16Mp3,3Lfys64Lfx96Lrx96Lfx192O1c1], flags=41, iteration=2457900, sample_iteration=2458041, null_char=91, learning_rate=0.001, momentum=0.5, adam_beta=0.999

Version string:4.00.00alpha:glg:synth20170629
LSTM training info:Network str:[1,48,0,1Ct3,3,16Mp3,3Lfys64Lfx96Lrx96Lfx512O1c1], flags=41, iteration=2711300, sample_iteration=2711543, null_char=97, learning_rate=0.001, momentum=0.5, adam_beta=0.999

Version string:4.00.00alpha:grc:synth20170629
LSTM training info:Network str:[1,48,0,1Ct3,3,16Mp3,3Lfys64Lfx96Lrx96Lfx192O1c1], flags=41, iteration=3843500, sample_iteration=3843646, null_char=211, learning_rate=0.001, momentum=0.5, adam_beta=0.999

Version string:4.00.00alpha:Greek:synth20170629
LSTM training info:Network str:[1,36,0,1Ct3,3,16Mp3,3Lfys48Lfx96Lrx96Lfx128O1c1], flags=41, iteration=8909600, sample_iteration=8909880, null_char=236, learning_rate=0.001, momentum=0.5, adam_beta=0.999

Version string:4.00.00alpha:Gujarati:synth20170629
LSTM training info:Network str:[1,36,0,1Ct3,3,16Mp3,3Lfys64Lfx96Lrx96Lfx128O1c1], flags=41, iteration=6433600, sample_iteration=6434873, null_char=2, learning_rate=0.001, momentum=0.5, adam_beta=0.999

Version string:4.00.00alpha:guj:synth20170629
LSTM training info:Network str:[1,48,0,1Ct3,3,16Mp3,3Lfys64Lfx96Lrx96Lfx192O1c1], flags=41, iteration=1609800, sample_iteration=1609975, null_char=2, learning_rate=0.001, momentum=0.5, adam_beta=0.999

Version string:4.00.00alpha:Gurmukhi:synth20170629
LSTM training info:Network str:[1,36,0,1Ct3,3,16Mp3,3Lfys48Lfx96Lrx96Lfx128O1c1], flags=41, iteration=7659800, sample_iteration=7660645, null_char=2, learning_rate=0.001, momentum=0.5, adam_beta=0.999

Version string:4.00.00alpha:Hangul:synth20170629
LSTM training info:Network str:[1,48,0,1Ct3,3,16Mp3,3Lfys64Lfx96Lrx96Lfx192O1c1], flags=41, iteration=2103800, sample_iteration=2103883, null_char=210, learning_rate=0.001, momentum=0.5, adam_beta=0.999

Version string:4.00.00alpha:Hangul_vert:synth20170629
LSTM training info:Network str:[1,36,0,1Ct3,3,16Mp3,3Lfys64Lfx96Lrx96Lfx128O1c1], flags=41, iteration=5218300, sample_iteration=5220005, null_char=213, learning_rate=0.001, momentum=0.5, adam_beta=0.999

Version string:4.00.00alpha:HanS:synth20170629:[1,48,0,1Ct3,3,16Mp3,3Lfys64Lfx96Lrx96Lfx512O1c1]
LSTM training info:Network str:[1,48,0,1Ct3,3,16Mp3,3Lfys64Lfx96Lrx96Lfx512O1c1], flags=41, iteration=2009700, sample_iteration=2013398, null_char=238, learning_rate=0.001, momentum=0.5, adam_beta=0.999

Version string:4.00.00alpha:HanS_vert:synth20170629
LSTM training info:Network str:[1,48,0,1Ct3,3,16Mp3,3Lfys64Lfx96Lrx96Lfx384O1c1], flags=41, iteration=2966600, sample_iteration=2977655, null_char=238, learning_rate=0.001, momentum=0.5, adam_beta=0.999

Version string:4.00.00alpha:HanT:synth20170629
LSTM training info:Network str:[1,48,0,1Ct3,3,16Mp3,3Lfys64Lfx96Lrx96Lfx384O1c1], flags=41, iteration=2342300, sample_iteration=2346092, null_char=240, learning_rate=0.001, momentum=0.5, adam_beta=0.999

Version string:4.00.00alpha:HanT_vert:synth20170629
LSTM training info:Network str:[1,36,0,1Ct3,3,16Mp3,3Lfys64Lfx96Lrx96Lfx384O1c1], flags=41, iteration=4202000, sample_iteration=4241091, null_char=240, learning_rate=0.001, momentum=0.5, adam_beta=0.999

Version string:4.00.00alpha:hat:synth20170629
LSTM training info:Network str:[1,36,0,1Ct3,3,16Mp3,3Lfys64Lfx96Lrx96Lfx512O1c1], flags=41, iteration=2653800, sample_iteration=2653890, null_char=96, learning_rate=0.001, momentum=0.5, adam_beta=0.999

Version string:4.00.00alpha:Hebrew:synth20170629:[1,36,0,1Ct3,3,16Mp3,3Lfys48Lfx96Lrx96Lfx128O1c1]
LSTM training info:Network str:[1,36,0,1Ct3,3,16Mp3,3Lfys48Lfx96Lrx96Lfx128O1c1], flags=41, iteration=4137300, sample_iteration=4140116, null_char=2, learning_rate=0.001, momentum=0.5, adam_beta=0.999

Version string:4.00.00alpha:heb:synth20170629:[1,36,0,1Ct3,3,16Mp3,3Lfys48Lfx96Lrx96Lfx128O1c1]
LSTM training info:Network str:[1,36,0,1Ct3,3,16Mp3,3Lfys48Lfx96Lrx96Lfx128O1c1], flags=41, iteration=3399600, sample_iteration=3405090, null_char=2, learning_rate=0.001, momentum=0.5, adam_beta=0.999

Version string:4.00.00alpha:hin:synth20170629
LSTM training info:Network str:[1,48,0,1Ct3,3,16Mp3,3Lfys64Lfx96Lrx96Lfx384O1c1], flags=41, iteration=2736900, sample_iteration=2737076, null_char=2, learning_rate=0.001, momentum=0.5, adam_beta=0.999

Version string:4.00.00alpha:hrv:synth20170629:[1,36,0,1Ct3,3,16Mp3,3Lfys48Lfx96Lrx96Lfx192O1c1]
LSTM training info:Network str:[1,36,0,1Ct3,3,16Mp3,3Lfys48Lfx96Lrx96Lfx192O1c1], flags=41, iteration=2723200, sample_iteration=2723414, null_char=105, learning_rate=0.001, momentum=0.5, adam_beta=0.999

Version string:4.00.00alpha:hun:synth20170629:[1,48,0,1Ct3,3,16Mp3,3Lfys64Lfx96Lrx96Lfx192O1c1]
LSTM training info:Network str:[1,48,0,1Ct3,3,16Mp3,3Lfys64Lfx96Lrx96Lfx192O1c1], flags=41, iteration=3443300, sample_iteration=3443765, null_char=97, learning_rate=0.001, momentum=0.5, adam_beta=0.999

Version string:4.00.00alpha:hye:synth20170629:[1,36,0,1Ct3,3,16Mp3,3Lfys48Lfx96Lrx96Lfx128O1c1]
LSTM training info:Network str:[1,36,0,1Ct3,3,16Mp3,3Lfys48Lfx96Lrx96Lfx128O1c1], flags=41, iteration=5222400, sample_iteration=5224599, null_char=104, learning_rate=0.001, momentum=0.5, adam_beta=0.999

Version string:4.00.00alpha:iku:synth20170629
LSTM training info:Network str:[1,36,0,1Ct3,3,16Mp3,3Lfys48Lfx96Lrx96Lfx192O1c1], flags=41, iteration=3862400, sample_iteration=3862672, null_char=595, learning_rate=0.001, momentum=0.5, adam_beta=0.999

Version string:4.00.00alpha:ind:synth20170629:[1,36,0,1Ct3,3,16Mp3,3Lfys64Lfx96Lrx96Lfx128O1c1]
LSTM training info:Network str:[1,36,0,1Ct3,3,16Mp3,3Lfys64Lfx96Lrx96Lfx128O1c1], flags=41, iteration=4643300, sample_iteration=4643534, null_char=84, learning_rate=0.001, momentum=0.5, adam_beta=0.999

Version string:4.00.00alpha:isl:synth20170629:[1,36,0,1Ct3,3,16Mp3,3Lfys64Lfx96Lrx96Lfx128O1c1]
LSTM training info:Network str:[1,36,0,1Ct3,3,16Mp3,3Lfys64Lfx96Lrx96Lfx128O1c1], flags=41, iteration=1463300, sample_iteration=1463419, null_char=110, learning_rate=0.001, momentum=0.5, adam_beta=0.999

Version string:4.00.00alpha:ita_old:synth20170629
LSTM training info:Network str:[1,48,0,1Ct3,3,16Mp3,3Lfys64Lfx96Lrx96Lfx384O1c1], flags=41, iteration=2975300, sample_iteration=2980533, null_char=117, learning_rate=0.001, momentum=0.5, adam_beta=0.999

Version string:4.00.00alpha:ita:synth20170629
LSTM training info:Network str:[1,36,0,1Ct3,3,16Mp3,3Lfys64Lfx96Lrx96Lfx192O1c1], flags=41, iteration=5146400, sample_iteration=5146726, null_char=118, learning_rate=0.001, momentum=0.5, adam_beta=0.999

Version string:4.00.00alpha:Japanese:synth20170629
LSTM training info:Network str:[1,48,0,1Ct3,3,16Mp3,3Lfys64Lfx96Lrx96Lfx384O1c1], flags=41, iteration=2937400, sample_iteration=2940965, null_char=429, learning_rate=0.001, momentum=0.5, adam_beta=0.999

Version string:4.00.00alpha:Japanese_vert:synth20170629:[1,36,0,1Ct3,3,16Mp3,3Lfys64Lfx96Lrx96Lfx512O1c1]
LSTM training info:Network str:[1,36,0,1Ct3,3,16Mp3,3Lfys64Lfx96Lrx96Lfx512O1c1], flags=41, iteration=2510500, sample_iteration=2514591, null_char=429, learning_rate=0.001, momentum=0.5, adam_beta=0.999

Version string:4.00.00alpha:jav:synth20170629
LSTM training info:Network str:[1,48,0,1Ct3,3,16Mp3,3Lfys64Lfx64Lrx64Lfx384O1c1], flags=41, iteration=449600, sample_iteration=449630, null_char=92, learning_rate=0.001, momentum=0.5, adam_beta=0.999

Version string:4.00.00alpha:jpn:synth20170629:[1,36,0,1Ct3,3,16Mp3,3Lfys64Lfx96Lrx96Lfx384O1c1]
LSTM training info:Network str:[1,36,0,1Ct3,3,16Mp3,3Lfys64Lfx96Lrx96Lfx384O1c1], flags=41, iteration=3261700, sample_iteration=3267677, null_char=414, learning_rate=0.001, momentum=0.5, adam_beta=0.999

Version string:4.00.00alpha:jpn_vert:synth20170629:[1,48,0,1Ct3,3,16Mp3,3Lfys64Lfx96Lrx96Lfx512O1c1]
LSTM training info:Network str:[1,48,0,1Ct3,3,16Mp3,3Lfys64Lfx96Lrx96Lfx512O1c1], flags=41, iteration=1874000, sample_iteration=1878622, null_char=414, learning_rate=0.001, momentum=0.5, adam_beta=0.999

Version string:4.00.00alpha:Kannada:synth20170629
LSTM training info:Network str:[1,36,0,1Ct3,3,16Mp3,3Lfys64Lfx96Lrx96Lfx192O1c1], flags=41, iteration=882600, sample_iteration=882910, null_char=2, learning_rate=0.001, momentum=0.5, adam_beta=0.999

Version string:4.00.00alpha:kan:synth20170629:[1,36,0,1Ct3,3,16Mp3,3Lfys64Lfx96Lrx96Lfx384O1c1]
LSTM training info:Network str:[1,36,0,1Ct3,3,16Mp3,3Lfys64Lfx96Lrx96Lfx384O1c1], flags=41, iteration=2217600, sample_iteration=2219122, null_char=2, learning_rate=0.001, momentum=0.5, adam_beta=0.999

Version string:4.00.00alpha:kat_old:synth20170629
LSTM training info:Network str:[1,36,0,1Ct3,3,16Mp3,3Lfys64Lfx96Lrx96Lfx192O1c1], flags=41, iteration=6695800, sample_iteration=6695849, null_char=84, learning_rate=0.001, momentum=0.5, adam_beta=0.999

Version string:4.00.00alpha:kat:synth20170629
LSTM training info:Network str:[1,48,0,1Ct3,3,16Mp3,3Lfys64Lfx96Lrx96Lfx128O1c1], flags=41, iteration=5277000, sample_iteration=5286853, null_char=78, learning_rate=0.001, momentum=0.5, adam_beta=0.999

Version string:4.00.00alpha:kaz:synth20170629
LSTM training info:Network str:[1,36,0,1Ct3,3,16Mp3,3Lfys64Lfx96Lrx96Lfx192O1c1], flags=41, iteration=3952100, sample_iteration=3952887, null_char=116, learning_rate=0.001, momentum=0.5, adam_beta=0.999

Version string:4.00.00alpha:Khmer:synth20170629
LSTM training info:Network str:[1,36,0,1Ct3,3,16Mp3,3Lfys48Lfx96Lrx96Lfx128O1c1], flags=41, iteration=8292700, sample_iteration=8393977, null_char=2, learning_rate=0.001, momentum=0.5, adam_beta=0.999

Version string:4.00.00alpha:khm:synth20170629:[1,48,0,1Ct3,3,16Mp3,3Lfys64Lfx96Lrx96Lfx384O1c1]
LSTM training info:Network str:[1,48,0,1Ct3,3,16Mp3,3Lfys64Lfx96Lrx96Lfx384O1c1], flags=41, iteration=2208100, sample_iteration=2250468, null_char=2, learning_rate=0.001, momentum=0.5, adam_beta=0.999

Version string:4.00.00alpha:kir:synth20170629
LSTM training info:Network str:[1,48,0,1Ct3,3,16Mp3,3Lfys64Lfx96Lrx96Lfx128O1c1], flags=41, iteration=5271100, sample_iteration=5274339, null_char=142, learning_rate=0.001, momentum=0.5, adam_beta=0.999

Version string:4.00.00alpha:kor:synth20170629:[1,48,0,1Ct3,3,16Mp3,3Lfys64Lfx96Lrx96Lfx384O1c1]
LSTM training info:Network str:[1,48,0,1Ct3,3,16Mp3,3Lfys64Lfx96Lrx96Lfx384O1c1], flags=41, iteration=1458300, sample_iteration=1458333, null_char=143, learning_rate=0.001, momentum=0.5, adam_beta=0.999

Version string:4.00.00alpha:kor_vert:synth20170629:[1,36,0,1Ct3,3,16Mp3,3Lfys48Lfx96Lrx96Lfx192O1c1]
LSTM training info:Network str:[1,36,0,1Ct3,3,16Mp3,3Lfys48Lfx96Lrx96Lfx192O1c1], flags=41, iteration=1357200, sample_iteration=1359703, null_char=147, learning_rate=0.001, momentum=0.5, adam_beta=0.999

Version string:4.00.00alpha:kur_ara:synth20170629
LSTM training info:Network str:[1,48,0,1Ct3,3,16Mp3,3Lfys64Lfx96Lrx96Lfx384O1c1], flags=41, iteration=2729500, sample_iteration=2731777, null_char=2, learning_rate=0.001, momentum=0.5, adam_beta=0.999

Version string:4.00.00alpha:lao:synth20170629:[1,36,0,1Ct3,3,16Mp3,3Lfys48Lfx96Lrx96Lfx128O1c1]
LSTM training info:Network str:[1,36,0,1Ct3,3,16Mp3,3Lfys48Lfx96Lrx96Lfx128O1c1], flags=41, iteration=1887800, sample_iteration=1891645, null_char=2, learning_rate=0.001, momentum=0.5, adam_beta=0.999

Version string:4.00.00alpha:Lao:synth20170629
LSTM training info:Network str:[1,36,0,1Ct3,3,16Mp3,3Lfys48Lfx96Lrx96Lfx128O1c1], flags=41, iteration=6606700, sample_iteration=6614442, null_char=2, learning_rate=0.001, momentum=0.5, adam_beta=0.999

Version string:4.00.00alpha:Latin:synth20170629
LSTM training info:Network str:[1,48,0,1Ct3,3,16Mp3,3Lfys64Lfx96Lrx96Lfx192O1c1], flags=41, iteration=3353000, sample_iteration=3353210, null_char=301, learning_rate=0.001, momentum=0.5, adam_beta=0.999

Version string:4.00.00alpha:lat:synth20170629
LSTM training info:Network str:[1,36,0,1Ct3,3,16Mp3,3Lfys64Lfx96Lrx96Lfx384O1c1], flags=41, iteration=2768500, sample_iteration=2768698, null_char=99, learning_rate=0.001, momentum=0.5, adam_beta=0.999

Version string:4.00.00alpha:lav:synth20170629:[1,36,0,1Ct3,3,16Mp3,3Lfys64Lfx96Lrx96Lfx128O1c1]
LSTM training info:Network str:[1,36,0,1Ct3,3,16Mp3,3Lfys64Lfx96Lrx96Lfx128O1c1], flags=41, iteration=6526700, sample_iteration=6527341, null_char=113, learning_rate=0.001, momentum=0.5, adam_beta=0.999

Version string:4.00.00alpha:lit:synth20170629:[1,36,0,1Ct3,3,16Mp3,3Lfys48Lfx96Lrx96Lfx192O1c1]
LSTM training info:Network str:[1,36,0,1Ct3,3,16Mp3,3Lfys48Lfx96Lrx96Lfx192O1c1], flags=41, iteration=1190000, sample_iteration=1190081, null_char=107, learning_rate=0.001, momentum=0.5, adam_beta=0.999

Version string:4.00.00alpha:ltz:synth20170629
LSTM training info:Network str:[1,36,0,1Ct3,3,16Mp3,3Lfys64Lfx96Lrx96Lfx512O1c1], flags=41, iteration=16600, sample_iteration=16602, null_char=86, learning_rate=0.001, momentum=0.5, adam_beta=0.999

Version string:4.00.00alpha:Malayalam:synth20170629:[1,36,0,1Ct3,3,16Mp3,3Lfys64Lfx96Lrx96Lfx128O1c1]
LSTM training info:Network str:[1,36,0,1Ct3,3,16Mp3,3Lfys64Lfx96Lrx96Lfx128O1c1], flags=41, iteration=3192300, sample_iteration=3194140, null_char=2, learning_rate=0.001, momentum=0.5, adam_beta=0.999

Version string:4.00.00alpha:mal:synth20170629:[1,36,0,1Ct3,3,16Mp3,3Lfys48Lfx96Lrx96Lfx128O1c1]
LSTM training info:Network str:[1,36,0,1Ct3,3,16Mp3,3Lfys48Lfx96Lrx96Lfx128O1c1], flags=41, iteration=591500, sample_iteration=592095, null_char=2, learning_rate=0.001, momentum=0.5, adam_beta=0.999

Version string:4.00.00alpha:mar:synth20170629
LSTM training info:Network str:[1,48,0,1Ct3,3,16Mp3,3Lfys64Lfx96Lrx96Lfx192O1c1], flags=41, iteration=3278000, sample_iteration=3278243, null_char=2, learning_rate=0.001, momentum=0.5, adam_beta=0.999

Version string:4.00.00alpha:mkd:synth20170629:[1,36,0,1Ct3,3,16Mp3,3Lfys64Lfx96Lrx96Lfx192O1c1]
LSTM training info:Network str:[1,36,0,1Ct3,3,16Mp3,3Lfys64Lfx96Lrx96Lfx192O1c1], flags=41, iteration=2341900, sample_iteration=2342274, null_char=83, learning_rate=0.001, momentum=0.5, adam_beta=0.999

Version string:4.00.00alpha:mlt:synth20170629
LSTM training info:Network str:[1,36,0,1Ct3,3,16Mp3,3Lfys64Lfx96Lrx96Lfx192O1c1], flags=41, iteration=4769500, sample_iteration=4770242, null_char=84, learning_rate=0.001, momentum=0.5, adam_beta=0.999

Version string:4.00.00alpha:mon:synth20170629
LSTM training info:Network str:[1,36,0,1Ct3,3,16Mp3,3Lfys64Lfx96Lrx96Lfx384O1c1], flags=41, iteration=3913100, sample_iteration=3913523, null_char=96, learning_rate=0.001, momentum=0.5, adam_beta=0.999

Version string:4.00.00alpha:mri:synth20170629
LSTM training info:Network str:[1,36,0,1Ct3,3,16Mp3,3Lfys64Lfx96Lrx96Lfx192O1c1], flags=41, iteration=6812500, sample_iteration=6812705, null_char=81, learning_rate=0.001, momentum=0.5, adam_beta=0.999

Version string:4.00.00alpha:msa:synth20170629:[1,48,0,1Ct3,3,16Mp3,3Lfys64Lfx96Lrx96Lfx384O1c1]
LSTM training info:Network str:[1,48,0,1Ct3,3,16Mp3,3Lfys64Lfx96Lrx96Lfx384O1c1], flags=41, iteration=1919100, sample_iteration=1919220, null_char=86, learning_rate=0.001, momentum=0.5, adam_beta=0.999

Version string:4.00.00alpha:Myanmar:synth20170629
LSTM training info:Network str:[1,48,0,1Ct3,3,16Mp3,3Lfys64Lfx96Lrx96Lfx384O1c1], flags=41, iteration=3179300, sample_iteration=3184457, null_char=2, learning_rate=0.001, momentum=0.5, adam_beta=0.999

Version string:4.00.00alpha:mya:synth20170629
LSTM training info:Network str:[1,48,0,1Ct3,3,16Mp3,3Lfys64Lfx96Lrx96Lfx512O1c1], flags=41, iteration=2609700, sample_iteration=2617837, null_char=2, learning_rate=0.001, momentum=0.5, adam_beta=0.999

Version string:4.00.00alpha:nep:synth20170629:[1,48,0,1Ct3,3,16Mp3,3Lfys64Lfx96Lrx96Lfx128O1c1]
LSTM training info:Network str:[1,48,0,1Ct3,3,16Mp3,3Lfys64Lfx96Lrx96Lfx128O1c1], flags=41, iteration=2913000, sample_iteration=2913772, null_char=2, learning_rate=0.001, momentum=0.5, adam_beta=0.999

Version string:4.00.00alpha:nld:synth20170629:[1,36,0,1Ct3,3,16Mp3,3Lfys48Lfx96Lrx96Lfx192O1c1]
LSTM training info:Network str:[1,36,0,1Ct3,3,16Mp3,3Lfys48Lfx96Lrx96Lfx192O1c1], flags=41, iteration=1233000, sample_iteration=1233084, null_char=149, learning_rate=0.001, momentum=0.5, adam_beta=0.999

Version string:4.00.00alpha:nor:synth20170629:[1,36,0,1Ct3,3,16Mp3,3Lfys64Lfx96Lrx96Lfx384O1c1]
LSTM training info:Network str:[1,36,0,1Ct3,3,16Mp3,3Lfys64Lfx96Lrx96Lfx384O1c1], flags=41, iteration=2363800, sample_iteration=2363942, null_char=103, learning_rate=0.001, momentum=0.5, adam_beta=0.999

Version string:4.00.00alpha:oci:synth20170629
LSTM training info:Network str:[1,48,0,1Ct3,3,16Mp3,3Lfys64Lfx96Lrx96Lfx384O1c1], flags=41, iteration=3059700, sample_iteration=3059833, null_char=128, learning_rate=0.001, momentum=0.5, adam_beta=0.999

Version string:4.00.00alpha:ori:synth20170629
LSTM training info:Network str:[1,48,0,1Ct3,3,16Mp3,3Lfys64Lfx96Lrx96Lfx384O1c1], flags=41, iteration=4023900, sample_iteration=4026843, null_char=2, learning_rate=0.001, momentum=0.5, adam_beta=0.999

Version string:4.00.00alpha:Oriya:synth20170629
LSTM training info:Network str:[1,48,0,1Ct3,3,16Mp3,3Lfys64Lfx96Lrx96Lfx512O1c1], flags=41, iteration=1636900, sample_iteration=1637404, null_char=2, learning_rate=0.001, momentum=0.5, adam_beta=0.999

Version string:4.00.00alpha:osd:synth20170629:[1,36,0,1Ct3,3,16Mp3,3Lfys64Lfx96Lrx96Lfx128O1c1]
LSTM training info:Network str:[1,36,0,1Ct3,3,16Mp3,3Lfys64Lfx96Lrx96Lfx128O1c1], flags=41, iteration=3724000, sample_iteration=3777456, null_char=2, learning_rate=0.001, momentum=0.5, adam_beta=0.999

Version string:4.00.00alpha:pan:synth20170629:[1,36,0,1Ct3,3,16Mp3,3Lfys48Lfx96Lrx96Lfx128O1c1]
LSTM training info:Network str:[1,36,0,1Ct3,3,16Mp3,3Lfys48Lfx96Lrx96Lfx128O1c1], flags=41, iteration=1331400, sample_iteration=1331667, null_char=2, learning_rate=0.001, momentum=0.5, adam_beta=0.999

Version string:4.00.00alpha:pol:synth20170629:[1,36,0,1Ct3,3,16Mp3,3Lfys64Lfx96Lrx96Lfx128O1c1]
LSTM training info:Network str:[1,36,0,1Ct3,3,16Mp3,3Lfys64Lfx96Lrx96Lfx128O1c1], flags=41, iteration=4037800, sample_iteration=4038310, null_char=112, learning_rate=0.001, momentum=0.5, adam_beta=0.999

Version string:4.00.00alpha:por:synth20170629
LSTM training info:Network str:[1,36,0,1Ct3,3,16Mp3,3Lfys48Lfx96Lrx96Lfx192O1c1], flags=41, iteration=1850300, sample_iteration=1850422, null_char=118, learning_rate=0.001, momentum=0.5, adam_beta=0.999

Version string:4.00.00alpha:pus:synth20170629
LSTM training info:Network str:[1,48,0,1Ct3,3,16Mp3,3Lfys64Lfx96Lrx96Lfx512O1c1], flags=41, iteration=2355400, sample_iteration=2358432, null_char=2, learning_rate=0.001, momentum=0.5, adam_beta=0.999

Version string:4.00.00alpha:que:synth20170629
LSTM training info:Network str:[1,48,0,1Ct3,3,16Mp3,3Lfys64Lfx64Lrx64Lfx384O1c1], flags=41, iteration=3950200, sample_iteration=3950594, null_char=122, learning_rate=0.001, momentum=0.5, adam_beta=0.999

Version string:4.00.00alpha:ron:synth20170629:[1,36,0,1Ct3,3,16Mp3,3Lfys48Lfx96Lrx96Lfx128O1c1]
LSTM training info:Network str:[1,36,0,1Ct3,3,16Mp3,3Lfys48Lfx96Lrx96Lfx128O1c1], flags=41, iteration=916200, sample_iteration=916276, null_char=109, learning_rate=0.001, momentum=0.5, adam_beta=0.999

Version string:4.00.00alpha:rus:synth20170629:[1,36,0,1Ct3,3,16Mp3,3Lfys64Lfx96Lrx96Lfx128O1c1]
LSTM training info:Network str:[1,36,0,1Ct3,3,16Mp3,3Lfys64Lfx96Lrx96Lfx128O1c1], flags=41, iteration=6081800, sample_iteration=6084626, null_char=123, learning_rate=0.001, momentum=0.5, adam_beta=0.999

Version string:4.00.00alpha:san:synth20170629
LSTM training info:Network str:[1,36,0,1Ct3,3,16Mp3,3Lfys48Lfx96Lrx96Lfx192O1c1], flags=41, iteration=200200, sample_iteration=200279, null_char=2, learning_rate=0.001, momentum=0.5, adam_beta=0.999

Version string:4.00.00alpha:Sinhala:synth20170629
LSTM training info:Network str:[1,48,0,1Ct3,3,16Mp3,3Lfys64Lfx96Lrx96Lfx128O1c1], flags=41, iteration=244600, sample_iteration=244610, null_char=2, learning_rate=0.001, momentum=0.5, adam_beta=0.999

Version string:4.00.00alpha:sin:synth20170629
LSTM training info:Network str:[1,48,0,1Ct3,3,16Mp3,3Lfys64Lfx96Lrx96Lfx384O1c1], flags=41, iteration=4268500, sample_iteration=4268756, null_char=2, learning_rate=0.001, momentum=0.5, adam_beta=0.999

Version string:4.00.00alpha:slk:synth20170629
LSTM training info:Network str:[1,36,0,1Ct3,3,16Mp3,3Lfys64Lfx96Lrx96Lfx192O1c1], flags=41, iteration=5441500, sample_iteration=5442289, null_char=118, learning_rate=0.001, momentum=0.5, adam_beta=0.999

Version string:4.00.00alpha:slv:synth20170629
LSTM training info:Network str:[1,36,0,1Ct3,3,16Mp3,3Lfys64Lfx96Lrx96Lfx128O1c1], flags=41, iteration=5751300, sample_iteration=5751826, null_char=91, learning_rate=0.001, momentum=0.5, adam_beta=0.999

Version string:4.00.00alpha:snd:synth20170629
LSTM training info:Network str:[1,48,0,1Ct3,3,16Mp3,3Lfys64Lfx96Lrx96Lfx512O1c1], flags=41, iteration=2550300, sample_iteration=2555328, null_char=2, learning_rate=0.001, momentum=0.5, adam_beta=0.999

Version string:4.00.00alpha:spa_old:synth20170629
LSTM training info:Network str:[1,48,0,1Ct3,3,16Mp3,3Lfys64Lfx96Lrx96Lfx384O1c1], flags=41, iteration=1844900, sample_iteration=1845568, null_char=123, learning_rate=0.001, momentum=0.5, adam_beta=0.999

Version string:4.00.00alpha:spa:synth20170629
LSTM training info:Network str:[1,36,0,1Ct3,3,16Mp3,3Lfys48Lfx96Lrx96Lfx192O1c1], flags=41, iteration=6514100, sample_iteration=6514491, null_char=107, learning_rate=0.001, momentum=0.5, adam_beta=0.999

Version string:4.00.00alpha:sqi:synth20170629
LSTM training info:Network str:[1,36,0,1Ct3,3,16Mp3,3Lfys48Lfx96Lrx96Lfx128O1c1], flags=41, iteration=6242300, sample_iteration=6242829, null_char=78, learning_rate=0.001, momentum=0.5, adam_beta=0.999

Version string:4.00.00alpha:srp_latn:synth20170629
LSTM training info:Network str:[1,48,0,1Ct3,3,16Mp3,3Lfys64Lfx96Lrx96Lfx384O1c1], flags=41, iteration=3226700, sample_iteration=3226895, null_char=111, learning_rate=0.001, momentum=0.5, adam_beta=0.999

Version string:4.00.00alpha:srp:synth20170629:[1,36,0,1Ct3,3,16Mp3,3Lfys48Lfx96Lrx96Lfx128O1c1]
LSTM training info:Network str:[1,36,0,1Ct3,3,16Mp3,3Lfys48Lfx96Lrx96Lfx128O1c1], flags=41, iteration=2332000, sample_iteration=2332252, null_char=101, learning_rate=0.001, momentum=0.5, adam_beta=0.999

Version string:4.00.00alpha:sun:synth20170629
LSTM training info:Network str:[1,48,0,1Ct3,3,16Mp3,3Lfys64Lfx96Lrx96Lfx192O1c1], flags=41, iteration=5572000, sample_iteration=5572210, null_char=93, learning_rate=0.001, momentum=0.5, adam_beta=0.999

Version string:4.00.00alpha:swa:synth20170629
LSTM training info:Network str:[1,48,0,1Ct3,3,16Mp3,3Lfys64Lfx96Lrx96Lfx192O1c1], flags=41, iteration=2668900, sample_iteration=2669094, null_char=81, learning_rate=0.001, momentum=0.5, adam_beta=0.999

Version string:4.00.00alpha:swe:synth20170629:[1,48,0,1Ct3,3,16Mp3,3Lfys64Lfx96Lrx96Lfx512O1c1]
LSTM training info:Network str:[1,48,0,1Ct3,3,16Mp3,3Lfys64Lfx96Lrx96Lfx512O1c1], flags=41, iteration=1803900, sample_iteration=1804028, null_char=98, learning_rate=0.001, momentum=0.5, adam_beta=0.999

Version string:4.00.00alpha:Syriac:synth20170629
LSTM training info:Network str:[1,48,0,1Ct3,3,16Mp3,3Lfys64Lfx64Lrx64Lfx512O1c1], flags=41, iteration=3512900, sample_iteration=3516598, null_char=2, learning_rate=0.001, momentum=0.5, adam_beta=0.999

Version string:4.00.00alpha:syr:synth20170629
LSTM training info:Network str:[1,48,0,1Ct3,3,16Mp3,3Lfys64Lfx96Lrx96Lfx512O1c1], flags=41, iteration=2731600, sample_iteration=2738621, null_char=2, learning_rate=0.001, momentum=0.5, adam_beta=0.999

Version string:4.00.00alpha:Tamil:synth20170629:[1,36,0,1Ct3,3,16Mp3,3Lfys64Lfx96Lrx96Lfx192O1c1]
LSTM training info:Network str:[1,36,0,1Ct3,3,16Mp3,3Lfys64Lfx96Lrx96Lfx192O1c1], flags=41, iteration=1497800, sample_iteration=1497936, null_char=2, learning_rate=0.001, momentum=0.5, adam_beta=0.999

Version string:4.00.00alpha:tam:synth20170629:[1,36,0,1Ct3,3,16Mp3,3Lfys48Lfx96Lrx96Lfx128O1c1]
LSTM training info:Network str:[1,36,0,1Ct3,3,16Mp3,3Lfys48Lfx96Lrx96Lfx128O1c1], flags=41, iteration=2116900, sample_iteration=2117148, null_char=2, learning_rate=0.001, momentum=0.5, adam_beta=0.999

Version string:4.00.00alpha:tat:synth20170629
LSTM training info:Network str:[1,36,0,1Ct3,3,16Mp3,3Lfys64Lfx96Lrx96Lfx384O1c1], flags=41, iteration=3975700, sample_iteration=3975926, null_char=97, learning_rate=0.001, momentum=0.5, adam_beta=0.999

Version string:4.00.00alpha:tel:synth20170629:[1,48,0,1Ct3,3,16Mp3,3Lfys64Lfx96Lrx96Lfx128O1c1]
LSTM training info:Network str:[1,48,0,1Ct3,3,16Mp3,3Lfys64Lfx96Lrx96Lfx128O1c1], flags=41, iteration=705200, sample_iteration=705553, null_char=2, learning_rate=0.001, momentum=0.5, adam_beta=0.999

Version string:4.00.00alpha:Telugu:synth20170629:[1,48,0,1Ct3,3,16Mp3,3Lfys64Lfx96Lrx96Lfx128O1c1]
LSTM training info:Network str:[1,48,0,1Ct3,3,16Mp3,3Lfys64Lfx96Lrx96Lfx128O1c1], flags=41, iteration=2673100, sample_iteration=2673794, null_char=2, learning_rate=0.001, momentum=0.5, adam_beta=0.999

Version string:4.00.00alpha:tgk:synth20170629
LSTM training info:Network str:[1,48,0,1Ct3,3,16Mp3,3Lfys64Lfx96Lrx96Lfx128O1c1], flags=41, iteration=4505600, sample_iteration=4505867, null_char=120, learning_rate=0.001, momentum=0.5, adam_beta=0.999

Version string:4.00.00alpha:Thaana:synth20170629
LSTM training info:Network str:[1,48,0,1Ct3,3,16Mp3,3Lfys64Lfx96Lrx96Lfx384O1c1], flags=41, iteration=3214500, sample_iteration=3217590, null_char=2, learning_rate=0.001, momentum=0.5, adam_beta=0.999

Version string:4.00.00alpha:Thai:synth20170629
LSTM training info:Network str:[1,48,0,1Ct3,3,16Mp3,3Lfys64Lfx96Lrx96Lfx192O1c1], flags=41, iteration=5339000, sample_iteration=5343543, null_char=2, learning_rate=0.001, momentum=0.5, adam_beta=0.999

Version string:4.00.00alpha:tha:synth20170629
LSTM training info:Network str:[1,48,0,1Ct3,3,16Mp3,3Lfys64Lfx96Lrx96Lfx384O1c1], flags=41, iteration=1895200, sample_iteration=1897798, null_char=2, learning_rate=0.001, momentum=0.5, adam_beta=0.999

Version string:4.00.00alpha:Tibetan:synth20170629
LSTM training info:Network str:[1,48,0,1Ct3,3,16Mp3,3Lfys64Lfx96Lrx96Lfx384O1c1], flags=41, iteration=3447300, sample_iteration=3450348, null_char=2, learning_rate=0.001, momentum=0.5, adam_beta=0.999

Version string:4.00.00alpha:tir:synth20170629
LSTM training info:Network str:[1,36,0,1Ct3,3,16Mp3,3Lfys48Lfx96Lrx96Lfx128O1c1], flags=41, iteration=10498000, sample_iteration=10498000, null_char=267, learning_rate=0.001, momentum=0.5, adam_beta=0.999

Version string:4.00.00alpha:ton:synth20170629
LSTM training info:Network str:[1,48,0,1Ct3,3,16Mp3,3Lfys64Lfx96Lrx96Lfx192O1c1], flags=41, iteration=4730800, sample_iteration=4730909, null_char=107, learning_rate=0.001, momentum=0.5, adam_beta=0.999

Version string:4.00.00alpha:tur:synth20170629:[1,36,0,1Ct3,3,16Mp3,3Lfys48Lfx96Lrx96Lfx128O1c1]
LSTM training info:Network str:[1,36,0,1Ct3,3,16Mp3,3Lfys48Lfx96Lrx96Lfx128O1c1], flags=41, iteration=2465600, sample_iteration=2465932, null_char=102, learning_rate=0.001, momentum=0.5, adam_beta=0.999

Version string:4.00.00alpha:uig:synth20170629
LSTM training info:Network str:[1,48,0,1Ct3,3,16Mp3,3Lfys64Lfx96Lrx96Lfx512O1c1], flags=41, iteration=2731200, sample_iteration=2737916, null_char=2, learning_rate=0.001, momentum=0.5, adam_beta=0.999

Version string:4.00.00alpha:ukr:synth20170629
LSTM training info:Network str:[1,36,0,1Ct3,3,16Mp3,3Lfys64Lfx96Lrx96Lfx192O1c1], flags=41, iteration=3513800, sample_iteration=3514620, null_char=90, learning_rate=0.001, momentum=0.5, adam_beta=0.999

Version string:4.00.00alpha:urd:synth20170629
LSTM training info:Network str:[1,48,0,1Ct3,3,16Mp3,3Lfys64Lfx96Lrx96Lfx384O1c1], flags=41, iteration=3927800, sample_iteration=3938775, null_char=2, learning_rate=0.001, momentum=0.5, adam_beta=0.999

Version string:4.00.00alpha:uzb_cyrl:synth20170629
LSTM training info:Network str:[1,36,0,1Ct3,3,16Mp3,3Lfys64Lfx96Lrx96Lfx192O1c1], flags=41, iteration=4993600, sample_iteration=4995772, null_char=92, learning_rate=0.001, momentum=0.5, adam_beta=0.999

Version string:4.00.00alpha:uzb:synth20170629
LSTM training info:Network str:[1,48,0,1Ct3,3,16Mp3,3Lfys64Lfx96Lrx96Lfx384O1c1], flags=41, iteration=3363200, sample_iteration=3363853, null_char=86, learning_rate=0.001, momentum=0.5, adam_beta=0.999

Version string:4.00.00alpha:Vietnamese:synth20170629:[1,36,0,1Ct3,3,16Mp3,3Lfys64Lfx96Lrx96Lfx512O1c1]
LSTM training info:Network str:[1,36,0,1Ct3,3,16Mp3,3Lfys64Lfx96Lrx96Lfx512O1c1], flags=41, iteration=1874300, sample_iteration=1874317, null_char=268, learning_rate=0.001, momentum=0.5, adam_beta=0.999

Version string:4.00.00alpha:vie:synth20170629:[1,36,0,1Ct3,3,16Mp3,3Lfys48Lfx96Lrx96Lfx192O1c1]
LSTM training info:Network str:[1,36,0,1Ct3,3,16Mp3,3Lfys48Lfx96Lrx96Lfx192O1c1], flags=41, iteration=2528700, sample_iteration=2528724, null_char=268, learning_rate=0.001, momentum=0.5, adam_beta=0.999

Version string:4.00.00alpha:yid:synth20170629:[1,36,0,1Ct3,3,16Mp3,3Lfys64Lfx96Lrx96Lfx128O1c1]
LSTM training info:Network str:[1,36,0,1Ct3,3,16Mp3,3Lfys64Lfx96Lrx96Lfx128O1c1], flags=41, iteration=2008300, sample_iteration=2009307, null_char=2, learning_rate=0.001, momentum=0.5, adam_beta=0.999

Version string:4.00.00alpha:yor:synth20170629
LSTM training info:Network str:[1,48,0,1Ct3,3,16Mp3,3Lfys64Lfx96Lrx96Lfx192O1c1], flags=41, iteration=4201700, sample_iteration=4201736, null_char=100, learning_rate=0.001, momentum=0.5, adam_beta=0.999


Version string:4.00.00alpha:afr:synth20170629:[1,36,0,1Ct3,3,16Mp3,3Lfys64Lfx96Lrx96Lfx512O1c1]
LSTM training info:Network str:[1,36,0,1Ct3,3,16Mp3,3Lfys64Lfx96Lrx96Lfx512O1c1], flags=40, iteration=286700, sample_iteration=286724, null_char=95, learning_rate=0.001, momentum=0.5, adam_beta=0.999

Version string:4.00.00alpha:amh:synth20170629
LSTM training info:Network str:[1,36,0,1Ct3,3,16Mp3,3Lfys48Lfx96Lrx96Lfx192O1c1], flags=40, iteration=6112200, sample_iteration=6112270, null_char=284, learning_rate=0.001, momentum=0.5, adam_beta=0.999

Version string:4.00.00alpha:Arabic:synth20170629
LSTM training info:Network str:[1,48,0,1Ct3,3,16Mp3,3Lfys64Lfx96Lrx96Lfx384O1c1], flags=40, iteration=2417900, sample_iteration=2421715, null_char=2, learning_rate=0.001, momentum=0.5, adam_beta=0.999

Version string:4.00.00alpha:ara:synth20170629:[1,48,0,1Ct3,3,16Mp3,3Lfys64Lfx96Lrx96Lfx512O1c1]
LSTM training info:Network str:[1,48,0,1Ct3,3,16Mp3,3Lfys64Lfx96Lrx96Lfx512O1c1], flags=40, iteration=2111400, sample_iteration=2120404, null_char=2, learning_rate=0.001, momentum=0.5, adam_beta=0.999

Version string:4.00.00alpha:Armenian:synth20170629
LSTM training info:Network str:[1,36,0,1Ct3,3,16Mp3,3Lfys64Lfx96Lrx96Lfx512O1c1], flags=40, iteration=1999200, sample_iteration=1999769, null_char=191, learning_rate=0.001, momentum=0.5, adam_beta=0.999

Version string:4.00.00alpha:asm:synth20170629
LSTM training info:Network str:[1,48,0,1Ct3,3,16Mp3,3Lfys64Lfx64Lrx64Lfx512O1c1], flags=40, iteration=2758500, sample_iteration=2758570, null_char=2, learning_rate=0.001, momentum=0.5, adam_beta=0.999

Version string:4.00.00alpha:aze_cyrl:synth20170629
LSTM training info:Network str:[1,36,0,1Ct3,3,16Mp3,3Lfys64Lfx96Lrx96Lfx192O1c1], flags=40, iteration=7665300, sample_iteration=7666563, null_char=88, learning_rate=0.001, momentum=0.5, adam_beta=0.999

Version string:4.00.00alpha:aze:synth20170629
LSTM training info:Network str:[1,36,0,1Ct3,3,16Mp3,3Lfys64Lfx96Lrx96Lfx192O1c1], flags=40, iteration=6760000, sample_iteration=6760858, null_char=88, learning_rate=0.001, momentum=0.5, adam_beta=0.999

Version string:4.00.00alpha:bel:synth20170629
LSTM training info:Network str:[1,48,0,1Ct3,3,16Mp3,3Lfys64Lfx96Lrx96Lfx384O1c1], flags=40, iteration=2014700, sample_iteration=2014972, null_char=95, learning_rate=0.001, momentum=0.5, adam_beta=0.999

Version string:4.00.00alpha:Bengali:synth20170629:[1,48,0,1Ct3,3,16Mp3,3Lfys64Lfx96Lrx96Lfx512O1c1]
LSTM training info:Network str:[1,48,0,1Ct3,3,16Mp3,3Lfys64Lfx96Lrx96Lfx512O1c1], flags=40, iteration=1118100, sample_iteration=1118153, null_char=2, learning_rate=0.001, momentum=0.5, adam_beta=0.999

Version string:4.00.00alpha:ben:synth20170629:[1,48,0,1Ct3,3,16Mp3,3Lfys64Lfx64Lrx64Lfx512O1c1]
LSTM training info:Network str:[1,48,0,1Ct3,3,16Mp3,3Lfys64Lfx64Lrx64Lfx512O1c1], flags=40, iteration=1534600, sample_iteration=1534685, null_char=2, learning_rate=0.001, momentum=0.5, adam_beta=0.999

Version string:4.00.00alpha:bod:synth20170629
LSTM training info:Network str:[1,48,0,1Ct3,3,16Mp3,3Lfys64Lfx96Lrx96Lfx384O1c1], flags=40, iteration=3513900, sample_iteration=3524222, null_char=2, learning_rate=0.001, momentum=0.5, adam_beta=0.999

Version string:4.00.00alpha:bos:synth20170629
LSTM training info:Network str:[1,48,0,1Ct3,3,16Mp3,3Lfys64Lfx96Lrx96Lfx192O1c1], flags=40, iteration=3258400, sample_iteration=3258771, null_char=95, learning_rate=0.001, momentum=0.5, adam_beta=0.999

Version string:4.00.00alpha:bre:synth20170629
LSTM training info:Network str:[1,48,0,1Ct3,3,16Mp3,3Lfys64Lfx64Lrx64Lfx512O1c1], flags=40, iteration=14000, sample_iteration=14000, null_char=124, learning_rate=0.001, momentum=0.5, adam_beta=0.999

Version string:4.00.00alpha:bul:synth20170629:[1,48,0,1Ct3,3,16Mp3,3Lfys64Lfx96Lrx96Lfx384O1c1]
LSTM training info:Network str:[1,48,0,1Ct3,3,16Mp3,3Lfys64Lfx96Lrx96Lfx384O1c1], flags=40, iteration=887500, sample_iteration=887807, null_char=92, learning_rate=0.001, momentum=0.5, adam_beta=0.999

Version string:4.00.00alpha:Canadian_Aboriginal:synth20170629
LSTM training info:Network str:[1,48,0,1Ct3,3,16Mp3,3Lfys64Lfx96Lrx96Lfx384O1c1], flags=40, iteration=1949300, sample_iteration=1949421, null_char=652, learning_rate=0.001, momentum=0.5, adam_beta=0.999

Version string:4.00.00alpha:cat:synth20170629:[1,36,0,1Ct3,3,16Mp3,3Lfys48Lfx96Lrx96Lfx192O1c1]
LSTM training info:Network str:[1,36,0,1Ct3,3,16Mp3,3Lfys48Lfx96Lrx96Lfx192O1c1], flags=40, iteration=2427200, sample_iteration=2427351, null_char=88, learning_rate=0.001, momentum=0.5, adam_beta=0.999

Version string:4.00.00alpha:ceb:synth20170629
LSTM training info:Network str:[1,36,0,1Ct3,3,16Mp3,3Lfys64Lfx96Lrx96Lfx192O1c1], flags=40, iteration=6718000, sample_iteration=6772655, null_char=73, learning_rate=0.001, momentum=0.5, adam_beta=0.999

Version string:4.00.00alpha:ces:synth20170629:[1,48,0,1Ct3,3,16Mp3,3Lfys64Lfx96Lrx96Lfx384O1c1]
LSTM training info:Network str:[1,48,0,1Ct3,3,16Mp3,3Lfys64Lfx96Lrx96Lfx384O1c1], flags=40, iteration=3211200, sample_iteration=3211404, null_char=121, learning_rate=0.001, momentum=0.5, adam_beta=0.999

Version string:4.00.00alpha:Cherokee:synth20170629
LSTM training info:Network str:[1,36,0,1Ct3,3,16Mp3,3Lfys64Lfx96Lrx96Lfx192O1c1], flags=40, iteration=7542100, sample_iteration=7542435, null_char=191, learning_rate=0.001, momentum=0.5, adam_beta=0.999

Version string:4.00.00alpha:chi_sim:synth20170629:[1,48,0,1Ct3,3,16Mp3,3Lfys64Lfx96Lrx96Lfx512O1c1]
LSTM training info:Network str:[1,48,0,1Ct3,3,16Mp3,3Lfys64Lfx96Lrx96Lfx512O1c1], flags=40, iteration=1971300, sample_iteration=1976813, null_char=223, learning_rate=0.001, momentum=0.5, adam_beta=0.999

Version string:4.00.00alpha:chi_sim_vert:synth20170629:[1,36,0,1Ct3,3,16Mp3,3Lfys64Lfx96Lrx96Lfx512O1c1]
LSTM training info:Network str:[1,36,0,1Ct3,3,16Mp3,3Lfys64Lfx96Lrx96Lfx512O1c1], flags=40, iteration=2335900, sample_iteration=2350219, null_char=223, learning_rate=0.001, momentum=0.5, adam_beta=0.999

Version string:4.00.00alpha:chi_tra:synth20170629:[1,48,0,1Ct3,3,16Mp3,3Lfys64Lfx96Lrx96Lfx512O1c1]
LSTM training info:Network str:[1,48,0,1Ct3,3,16Mp3,3Lfys64Lfx96Lrx96Lfx512O1c1], flags=40, iteration=1988000, sample_iteration=1992889, null_char=226, learning_rate=0.001, momentum=0.5, adam_beta=0.999

Version string:4.00.00alpha:chi_tra_vert:synth20170629
LSTM training info:Network str:[1,36,0,1Ct3,3,16Mp3,3Lfys64Lfx96Lrx96Lfx512O1c1], flags=40, iteration=3521300, sample_iteration=3571821, null_char=226, learning_rate=0.001, momentum=0.5, adam_beta=0.999

Version string:4.00.00alpha:chr:synth20170629
LSTM training info:Network str:[1,36,0,1Ct3,3,16Mp3,3Lfys48Lfx96Lrx96Lfx128O1c1], flags=40, iteration=7847200, sample_iteration=7847486, null_char=102, learning_rate=0.001, momentum=0.5, adam_beta=0.999

Version string:4.00.00alpha:cos:synth20170629
LSTM training info:Network str:[1,36,0,1Ct3,3,16Mp3,3Lfys64Lfx96Lrx96Lfx384O1c1], flags=40, iteration=5120400, sample_iteration=5120693, null_char=104, learning_rate=0.001, momentum=0.5, adam_beta=0.999

Version string:4.00.00alpha:cym:synth20170629
LSTM training info:Network str:[1,36,0,1Ct3,3,16Mp3,3Lfys64Lfx96Lrx96Lfx384O1c1], flags=40, iteration=4212000, sample_iteration=4212285, null_char=108, learning_rate=0.001, momentum=0.5, adam_beta=0.999

Version string:4.00.00alpha:Cyrillic:synth20170629:[1,36,0,1Ct3,3,16Mp3,3Lfys64Lfx96Lrx96Lfx384O1c1]
LSTM training info:Network str:[1,36,0,1Ct3,3,16Mp3,3Lfys64Lfx96Lrx96Lfx384O1c1], flags=40, iteration=3121900, sample_iteration=3122619, null_char=202, learning_rate=0.001, momentum=0.5, adam_beta=0.999

Version string:4.00.00alpha:dan:synth20170629:[1,36,0,1Ct3,3,16Mp3,3Lfys64Lfx96Lrx96Lfx384O1c1]
LSTM training info:Network str:[1,36,0,1Ct3,3,16Mp3,3Lfys64Lfx96Lrx96Lfx384O1c1], flags=40, iteration=2547300, sample_iteration=2547538, null_char=100, learning_rate=0.001, momentum=0.5, adam_beta=0.999

Version string:4.00.00alpha:deu:synth20170629
LSTM training info:Network str:[1,48,0,1Ct3,3,16Mp3,3Lfys64Lfx96Lrx96Lfx384O1c1], flags=40, iteration=3543300, sample_iteration=3543653, null_char=114, learning_rate=0.001, momentum=0.5, adam_beta=0.999

Version string:4.00.00alpha:Devanagari:synth20170629
LSTM training info:Network str:[1,48,0,1Ct3,3,16Mp3,3Lfys64Lfx64Lrx64Lfx512O1c1], flags=40, iteration=2475100, sample_iteration=2475272, null_char=2, learning_rate=0.001, momentum=0.5, adam_beta=0.999

Version string:4.00.00alpha:div:synth20170629
LSTM training info:Network str:[1,48,0,1Ct3,3,16Mp3,3Lfys64Lfx96Lrx96Lfx192O1c1], flags=40, iteration=3249400, sample_iteration=3256730, null_char=2, learning_rate=0.001, momentum=0.5, adam_beta=0.999

Version string:4.00.00alpha:dzo:synth20170629
LSTM training info:Network str:[1,48,0,1Ct3,3,16Mp3,3Lfys64Lfx96Lrx96Lfx192O1c1], flags=40, iteration=4258800, sample_iteration=4335799, null_char=2, learning_rate=0.001, momentum=0.5, adam_beta=0.999

Version string:4.00.00alpha:ell:synth20170629
LSTM training info:Network str:[1,36,0,1Ct3,3,16Mp3,3Lfys64Lfx96Lrx96Lfx384O1c1], flags=40, iteration=3335500, sample_iteration=3335569, null_char=213, learning_rate=0.001, momentum=0.5, adam_beta=0.999

Version string:4.00.00alpha:eng:synth20170629:[1,36,0,1Ct3,3,16Mp3,3Lfys64Lfx96Lrx96Lfx512O1c1]
LSTM training info:Network str:[1,36,0,1Ct3,3,16Mp3,3Lfys64Lfx96Lrx96Lfx512O1c1], flags=40, iteration=814100, sample_iteration=814136, null_char=110, learning_rate=0.001, momentum=0.5, adam_beta=0.999

Version string:4.00.00alpha:enm:synth20170629
LSTM training info:Network str:[1,36,0,1Ct3,3,16Mp3,3Lfys64Lfx96Lrx96Lfx512O1c1], flags=40, iteration=2720200, sample_iteration=2721910, null_char=104, learning_rate=0.001, momentum=0.5, adam_beta=0.999

Version string:4.00.00alpha:epo:synth20170629
LSTM training info:Network str:[1,36,0,1Ct3,3,16Mp3,3Lfys48Lfx96Lrx96Lfx192O1c1], flags=40, iteration=6842600, sample_iteration=6843069, null_char=101, learning_rate=0.001, momentum=0.5, adam_beta=0.999

Version string:4.00.00alpha:est:synth20170629:[1,48,0,1Ct3,3,16Mp3,3Lfys64Lfx96Lrx96Lfx512O1c1]
LSTM training info:Network str:[1,48,0,1Ct3,3,16Mp3,3Lfys64Lfx96Lrx96Lfx512O1c1], flags=40, iteration=1637300, sample_iteration=1637435, null_char=103, learning_rate=0.001, momentum=0.5, adam_beta=0.999

Version string:4.00.00alpha:Ethiopic:synth20170629
LSTM training info:Network str:[1,36,0,1Ct3,3,16Mp3,3Lfys48Lfx96Lrx96Lfx128O1c1], flags=40, iteration=149100, sample_iteration=149101, null_char=385, learning_rate=0.001, momentum=0.5, adam_beta=0.999

Version string:4.00.00alpha:eus:synth20170629
LSTM training info:Network str:[1,36,0,1Ct3,3,16Mp3,3Lfys64Lfx96Lrx96Lfx192O1c1], flags=40, iteration=15200, sample_iteration=15204, null_char=89, learning_rate=0.001, momentum=0.5, adam_beta=0.999

Version string:4.00.00alpha:fao:synth20170629
LSTM training info:Network str:[1,48,0,1Ct3,3,16Mp3,3Lfys64Lfx96Lrx96Lfx384O1c1], flags=40, iteration=2812800, sample_iteration=2812950, null_char=126, learning_rate=0.001, momentum=0.5, adam_beta=0.999

Version string:4.00.00alpha:fas:synth20170629:[1,48,0,1Ct3,3,16Mp3,3Lfys64Lfx96Lrx96Lfx192O1c1]
LSTM training info:Network str:[1,48,0,1Ct3,3,16Mp3,3Lfys64Lfx96Lrx96Lfx192O1c1], flags=40, iteration=896400, sample_iteration=897843, null_char=2, learning_rate=0.001, momentum=0.5, adam_beta=0.999

Version string:4.00.00alpha:fil:synth20170629
LSTM training info:Network str:[1,36,0,1Ct3,3,16Mp3,3Lfys64Lfx96Lrx96Lfx384O1c1], flags=40, iteration=3854100, sample_iteration=3854348, null_char=81, learning_rate=0.001, momentum=0.5, adam_beta=0.999

Version string:4.00.00alpha:fin:synth20170629
LSTM training info:Network str:[1,36,0,1Ct3,3,16Mp3,3Lfys64Lfx96Lrx96Lfx384O1c1], flags=40, iteration=3741900, sample_iteration=3742321, null_char=94, learning_rate=0.001, momentum=0.5, adam_beta=0.999

Version string:4.00.00alpha:Fraktur:synth20170629
LSTM training info:Network str:[1,48,0,1Ct3,3,16Mp3,3Lfys64Lfx96Lrx96Lfx384O1c1], flags=40, iteration=3739900, sample_iteration=3740440, null_char=166, learning_rate=0.001, momentum=0.5, adam_beta=0.999

Version string:4.00.00alpha:fra:synth20170629
LSTM training info:Network str:[1,36,0,1Ct3,3,16Mp3,3Lfys48Lfx96Lrx96Lfx192O1c1], flags=40, iteration=3486400, sample_iteration=3486632, null_char=139, learning_rate=0.001, momentum=0.5, adam_beta=0.999

Version string:4.00.00alpha:frk:synth20170629
LSTM training info:Network str:[1,48,0,1Ct3,3,16Mp3,3Lfys64Lfx96Lrx96Lfx384O1c1], flags=40, iteration=3692700, sample_iteration=3692967, null_char=98, learning_rate=0.001, momentum=0.5, adam_beta=0.999

Version string:4.00.00alpha:frm:synth20170629
LSTM training info:Network str:[1,48,0,1Ct3,3,16Mp3,3Lfys64Lfx96Lrx96Lfx128O1c1], flags=40, iteration=176600, sample_iteration=176697, null_char=140, learning_rate=0.001, momentum=0.5, adam_beta=0.999

Version string:4.00.00alpha:fry:synth20170629
LSTM training info:Network str:[1,48,0,1Ct3,3,16Mp3,3Lfys64Lfx96Lrx96Lfx384O1c1], flags=40, iteration=3246500, sample_iteration=3246617, null_char=106, learning_rate=0.001, momentum=0.5, adam_beta=0.999

Version string:4.00.00alpha:Georgian:synth20170629
LSTM training info:Network str:[1,48,0,1Ct3,3,16Mp3,3Lfys64Lfx96Lrx96Lfx384O1c1], flags=40, iteration=2308600, sample_iteration=2310386, null_char=225, learning_rate=0.001, momentum=0.5, adam_beta=0.999

Version string:4.00.00alpha:gla:synth20170629
LSTM training info:Network str:[1,48,0,1Ct3,3,16Mp3,3Lfys64Lfx96Lrx96Lfx384O1c1], flags=40, iteration=3365500, sample_iteration=3365659, null_char=104, learning_rate=0.001, momentum=0.5, adam_beta=0.999

Version string:4.00.00alpha:gle:synth20170629
LSTM training info:Network str:[1,48,0,1Ct3,3,16Mp3,3Lfys64Lfx96Lrx96Lfx192O1c1], flags=40, iteration=2457900, sample_iteration=2458041, null_char=91, learning_rate=0.001, momentum=0.5, adam_beta=0.999

Version string:4.00.00alpha:glg:synth20170629
LSTM training info:Network str:[1,48,0,1Ct3,3,16Mp3,3Lfys64Lfx96Lrx96Lfx512O1c1], flags=40, iteration=2711300, sample_iteration=2711543, null_char=97, learning_rate=0.001, momentum=0.5, adam_beta=0.999

Version string:4.00.00alpha:grc:synth20170629
LSTM training info:Network str:[1,48,0,1Ct3,3,16Mp3,3Lfys64Lfx96Lrx96Lfx192O1c1], flags=40, iteration=3843500, sample_iteration=3843646, null_char=211, learning_rate=0.001, momentum=0.5, adam_beta=0.999

Version string:4.00.00alpha:Greek:synth20170629
LSTM training info:Network str:[1,36,0,1Ct3,3,16Mp3,3Lfys64Lfx96Lrx96Lfx384O1c1], flags=40, iteration=1727400, sample_iteration=1727456, null_char=236, learning_rate=0.001, momentum=0.5, adam_beta=0.999

Version string:4.00.00alpha:Gujarati:synth20170629
LSTM training info:Network str:[1,48,0,1Ct3,3,16Mp3,3Lfys64Lfx96Lrx96Lfx128O1c1], flags=40, iteration=4569600, sample_iteration=4569934, null_char=2, learning_rate=0.001, momentum=0.5, adam_beta=0.999

Version string:4.00.00alpha:guj:synth20170629:[1,36,0,1Ct3,3,16Mp3,3Lfys64Lfx96Lrx96Lfx384O1c1]
LSTM training info:Network str:[1,36,0,1Ct3,3,16Mp3,3Lfys64Lfx96Lrx96Lfx384O1c1], flags=40, iteration=1447700, sample_iteration=1448272, null_char=2, learning_rate=0.001, momentum=0.5, adam_beta=0.999

Version string:4.00.00alpha:Gurmukhi:synth20170629:[1,36,0,1Ct3,3,16Mp3,3Lfys64Lfx96Lrx96Lfx384O1c1]
LSTM training info:Network str:[1,36,0,1Ct3,3,16Mp3,3Lfys64Lfx96Lrx96Lfx384O1c1], flags=40, iteration=3177000, sample_iteration=3177347, null_char=2, learning_rate=0.001, momentum=0.5, adam_beta=0.999

Version string:4.00.00alpha:Hangul:synth20170629
LSTM training info:Network str:[1,48,0,1Ct3,3,16Mp3,3Lfys64Lfx96Lrx96Lfx384O1c1], flags=40, iteration=2510300, sample_iteration=2510401, null_char=210, learning_rate=0.001, momentum=0.5, adam_beta=0.999

Version string:4.00.00alpha:Hangul_vert:synth20170629:[1,48,0,1Ct3,3,16Mp3,3Lfys64Lfx96Lrx96Lfx512O1c1]
LSTM training info:Network str:[1,48,0,1Ct3,3,16Mp3,3Lfys64Lfx96Lrx96Lfx512O1c1], flags=40, iteration=881800, sample_iteration=882047, null_char=213, learning_rate=0.001, momentum=0.5, adam_beta=0.999

Version string:4.00.00alpha:HanS:synth20170629:[1,48,0,1Ct3,3,16Mp3,3Lfys64Lfx96Lrx96Lfx512O1c1]
LSTM training info:Network str:[1,48,0,1Ct3,3,16Mp3,3Lfys64Lfx96Lrx96Lfx512O1c1], flags=40, iteration=2009700, sample_iteration=2013398, null_char=238, learning_rate=0.001, momentum=0.5, adam_beta=0.999

Version string:4.00.00alpha:HanS_vert:synth20170629
LSTM training info:Network str:[1,48,0,1Ct3,3,16Mp3,3Lfys64Lfx96Lrx96Lfx384O1c1], flags=40, iteration=2966600, sample_iteration=2977655, null_char=238, learning_rate=0.001, momentum=0.5, adam_beta=0.999

Version string:4.00.00alpha:HanT:synth20170629
LSTM training info:Network str:[1,48,0,1Ct3,3,16Mp3,3Lfys64Lfx96Lrx96Lfx384O1c1], flags=40, iteration=2342300, sample_iteration=2346092, null_char=240, learning_rate=0.001, momentum=0.5, adam_beta=0.999

Version string:4.00.00alpha:HanT_vert:synth20170629:[1,48,0,1Ct3,3,16Mp3,3Lfys64Lfx96Lrx96Lfx384O1c1]
LSTM training info:Network str:[1,48,0,1Ct3,3,16Mp3,3Lfys64Lfx96Lrx96Lfx384O1c1], flags=40, iteration=2664100, sample_iteration=2686122, null_char=240, learning_rate=0.001, momentum=0.5, adam_beta=0.999

Version string:4.00.00alpha:hat:synth20170629
LSTM training info:Network str:[1,36,0,1Ct3,3,16Mp3,3Lfys64Lfx96Lrx96Lfx512O1c1], flags=40, iteration=2653800, sample_iteration=2653890, null_char=96, learning_rate=0.001, momentum=0.5, adam_beta=0.999

Version string:4.00.00alpha:Hebrew:synth20170629:[1,48,0,1Ct3,3,16Mp3,3Lfys64Lfx96Lrx96Lfx384O1c1]
LSTM training info:Network str:[1,48,0,1Ct3,3,16Mp3,3Lfys64Lfx96Lrx96Lfx384O1c1], flags=40, iteration=1902800, sample_iteration=1903513, null_char=2, learning_rate=0.001, momentum=0.5, adam_beta=0.999

Version string:4.00.00alpha:heb:synth20170629:[1,36,0,1Ct3,3,16Mp3,3Lfys48Lfx96Lrx96Lfx192O1c1]
LSTM training info:Network str:[1,36,0,1Ct3,3,16Mp3,3Lfys48Lfx96Lrx96Lfx192O1c1], flags=40, iteration=1568000, sample_iteration=1570525, null_char=2, learning_rate=0.001, momentum=0.5, adam_beta=0.999

Version string:4.00.00alpha:hin:synth20170629:[1,48,0,1Ct3,3,16Mp3,3Lfys64Lfx96Lrx96Lfx512O1c1]
LSTM training info:Network str:[1,48,0,1Ct3,3,16Mp3,3Lfys64Lfx96Lrx96Lfx512O1c1], flags=40, iteration=803600, sample_iteration=803651, null_char=2, learning_rate=0.001, momentum=0.5, adam_beta=0.999

Version string:4.00.00alpha:hrv:synth20170629:[1,36,0,1Ct3,3,16Mp3,3Lfys64Lfx96Lrx96Lfx384O1c1]
LSTM training info:Network str:[1,36,0,1Ct3,3,16Mp3,3Lfys64Lfx96Lrx96Lfx384O1c1], flags=40, iteration=4712800, sample_iteration=4713183, null_char=105, learning_rate=0.001, momentum=0.5, adam_beta=0.999

Version string:4.00.00alpha:hun:synth20170629:[1,48,0,1Ct3,3,16Mp3,3Lfys64Lfx96Lrx96Lfx384O1c1]
LSTM training info:Network str:[1,48,0,1Ct3,3,16Mp3,3Lfys64Lfx96Lrx96Lfx384O1c1], flags=40, iteration=2046400, sample_iteration=2046674, null_char=97, learning_rate=0.001, momentum=0.5, adam_beta=0.999

Version string:4.00.00alpha:hye:synth20170629:[1,36,0,1Ct3,3,16Mp3,3Lfys64Lfx96Lrx96Lfx192O1c1]
LSTM training info:Network str:[1,36,0,1Ct3,3,16Mp3,3Lfys64Lfx96Lrx96Lfx192O1c1], flags=40, iteration=1590800, sample_iteration=1591465, null_char=104, learning_rate=0.001, momentum=0.5, adam_beta=0.999

Version string:4.00.00alpha:iku:synth20170629
LSTM training info:Network str:[1,36,0,1Ct3,3,16Mp3,3Lfys48Lfx96Lrx96Lfx192O1c1], flags=40, iteration=3862400, sample_iteration=3862672, null_char=595, learning_rate=0.001, momentum=0.5, adam_beta=0.999

Version string:4.00.00alpha:ind:synth20170629:[1,48,0,1Ct3,3,16Mp3,3Lfys64Lfx96Lrx96Lfx384O1c1]
LSTM training info:Network str:[1,48,0,1Ct3,3,16Mp3,3Lfys64Lfx96Lrx96Lfx384O1c1], flags=40, iteration=876700, sample_iteration=876737, null_char=84, learning_rate=0.001, momentum=0.5, adam_beta=0.999

Version string:4.00.00alpha:isl:synth20170629:[1,36,0,1Ct3,3,16Mp3,3Lfys64Lfx96Lrx96Lfx384O1c1]
LSTM training info:Network str:[1,36,0,1Ct3,3,16Mp3,3Lfys64Lfx96Lrx96Lfx384O1c1], flags=40, iteration=2355200, sample_iteration=2355391, null_char=110, learning_rate=0.001, momentum=0.5, adam_beta=0.999

Version string:4.00.00alpha:ita_old:synth20170629
LSTM training info:Network str:[1,48,0,1Ct3,3,16Mp3,3Lfys64Lfx96Lrx96Lfx384O1c1], flags=40, iteration=2975300, sample_iteration=2980533, null_char=117, learning_rate=0.001, momentum=0.5, adam_beta=0.999

Version string:4.00.00alpha:ita:synth20170629:[1,48,0,1Ct3,3,16Mp3,3Lfys64Lfx64Lrx64Lfx384O1c1]
LSTM training info:Network str:[1,48,0,1Ct3,3,16Mp3,3Lfys64Lfx64Lrx64Lfx384O1c1], flags=40, iteration=1645500, sample_iteration=1645594, null_char=118, learning_rate=0.001, momentum=0.5, adam_beta=0.999

Version string:4.00.00alpha:Japanese:synth20170629:[1,48,0,1Ct3,3,16Mp3,3Lfys64Lfx96Lrx96Lfx512O1c1]
LSTM training info:Network str:[1,48,0,1Ct3,3,16Mp3,3Lfys64Lfx96Lrx96Lfx512O1c1], flags=40, iteration=1688700, sample_iteration=1690739, null_char=429, learning_rate=0.001, momentum=0.5, adam_beta=0.999

Version string:4.00.00alpha:Japanese_vert:synth20170629:[1,36,0,1Ct3,3,16Mp3,3Lfys64Lfx96Lrx96Lfx512O1c1]
LSTM training info:Network str:[1,36,0,1Ct3,3,16Mp3,3Lfys64Lfx96Lrx96Lfx512O1c1], flags=40, iteration=2510500, sample_iteration=2514591, null_char=429, learning_rate=0.001, momentum=0.5, adam_beta=0.999

Version string:4.00.00alpha:jav:synth20170629
LSTM training info:Network str:[1,48,0,1Ct3,3,16Mp3,3Lfys64Lfx64Lrx64Lfx384O1c1], flags=40, iteration=449600, sample_iteration=449630, null_char=92, learning_rate=0.001, momentum=0.5, adam_beta=0.999

Version string:4.00.00alpha:jpn:synth20170629:[1,48,0,1Ct3,3,16Mp3,3Lfys64Lfx96Lrx96Lfx512O1c1]
LSTM training info:Network str:[1,48,0,1Ct3,3,16Mp3,3Lfys64Lfx96Lrx96Lfx512O1c1], flags=40, iteration=2162500, sample_iteration=2166492, null_char=414, learning_rate=0.001, momentum=0.5, adam_beta=0.999

Version string:4.00.00alpha:jpn_vert:synth20170629:[1,48,0,1Ct3,3,16Mp3,3Lfys64Lfx96Lrx96Lfx512O1c1]
LSTM training info:Network str:[1,48,0,1Ct3,3,16Mp3,3Lfys64Lfx96Lrx96Lfx512O1c1], flags=40, iteration=1874000, sample_iteration=1878622, null_char=414, learning_rate=0.001, momentum=0.5, adam_beta=0.999

Version string:4.00.00alpha:Kannada:synth20170629:[1,48,0,1Ct3,3,16Mp
```

### quantized 'fast' models and the lang_map that was used to select them.

```
afr l36-64-96-512
ara l48-64-96-192
bel l36-48-96-128
ben l36-64-96-192
bul l36-48-96-128
...
```