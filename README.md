# AudioOnsetDetection

### The test dataset from:
Molina E , Tardon L J , Barbancho A M , et al. SiPTH: Singing Transcription Based on Hysteresis Defined on the Pitch-Time Curve[J]. IEEE/ACM Transactions on Audio, Speech, and Language Processing, 2015, 23(2):252-263.  
The onset detection only check the onset time in the ground-truth files  
### The train datase from:
Salamon J , Joan Serrà, Emilia Gómez. Tonal representations for music retrieval: From version identification to query-by-humming[J]. International Journal of Multimedia Information Retrieval, 2013.  
http://mtg.upf.edu/download/datasets/MTG-QBH

# Tips of onset detection.exe
cmd> onset_detection.exe *.wav  
output *csv file with time  
0.011  
1.222  
3.222


# Evaluation result
raw data of baseline and verification
                                          

Approach |precision |recall |f1-measure| 
|----| --- | --- | --- |
onset function(CNN) |0.646     |0.863  |0.732     |  
onset function(RNN) |0.711|0.686|0.671|
baseline            |0.414|0.922|0.564|
our CNN             |0.916|0.836|0.872|
our RNN             |0.915|0.850|0.880|
our LSTM            |0.926|0.850|0.885|

                    



##### onset function(CNN):  
[1]Musical Onset Detection with Convolutional Neural Networks” Jan Schlüter and Sebastian Böck. Proceedings of the 6th International Workshop on Machine Learning and Music, 2013.
##### onset function(RNN):  
[1]	“Universal Onset Detection with bidirectional Long Short-Term Memory Neural Networks” Florian Eyben, Sebastian Böck, Björn Schuller and Alex Graves. Proceedings of the 11th International Society for Music Information Retrieval Conference (ISMIR), 2010.  
[2]	“Online Real-time Onset Detection with Recurrent Neural Networks” Sebastian Böck, Andreas Arzt, Florian Krebs and Markus Schedl. Proceedings of the 15th International Conference on Digital Audio Effects (DAFx), 2012.  
##### our approach that add a verification step to the onset detection:  
baseline: modify the tradidtional peak-picking with sliding window because of post-processing  
our CNN,our RNN,our LSTM: training the network after the baseline. 

