# Slide:  
  * https://speech.ee.ntu.edu.tw/~hylee/ml/ml2021-course-data/seq2seq_v9.pdf  
# YT:  
  * https://www.youtube.com/watch?v=n9TlOhRjYoc  
  * https://www.youtube.com/watch?v=N6aRv06iv2g  
 
 ## Transformer  
 
  * Transformer is a Sequence-to-sequence(seq2seq) model.  
  * input: a sequence. output: a sequence.  
  * The output length is determined by model.  
  * Applications: Speech Recognition, Machine Translation and Speech Translation(Language without text).  

## Seq2seq2 for Chatbot  

 * input -> seq2seq2 -> response  

## Most Natural Language Processing applications...

 * most applications is Question Answering(QA)  
 * QA can be done by seq2seq2.  
 * ex. question, context -> seq2seq2 -> answer  
 * ref.: https://arxiv.org/abs/1806.08730 , https://arxiv.org/abs/1909.03329  
 * Applications:  
   * Sentiment analysis  
   * Write the abstract  
   * Language translation  
   * ...  
   
## seq2seq for Syntactic Parsing  
 * ref. Grammar as a Foreign Language  
 * ex.  
 * model input: deep learning is  very powerful.  
 * model output: (S (NP deep learning) (VP is (ADJV very powerful) ) )  

## seq2seq for multi-label classification  
 * an object can belong to multiple classes.  

## seq2seq for object detection  
 * ref. https://arxiv.org/abs/2005.12872  

## seq2seq overview  
 * input(sequence) -> Encoder -> Decoder -> output(sequence)  
 ![Image of Yaktocat](https://github.com/ting-chih/NTU-ML2021spring/blob/main/image/transformer.png)  


## Transformer - Encoder  
 * input: a vector, output: a vector.  
 * In the block,  
   * Input(a sequence vector) -> self-attention -> output(vector a)
   * Residual connection: output(vector a) + input(vector b)  
   * Vector(a+b) -> layer normalization -> vector(x)  
   * Vector(x) -> FC -> output + vector(x) -> layer normalization -> OUTPUT!!

 ![Image of Yaktocat](https://github.com/ting-chih/NTU-ML2021spring/blob/main/image/transformer-block.png)  
 ![Image of Yaktocat](https://github.com/ting-chih/NTU-ML2021spring/blob/main/image/blockexample.png)  
## Each element  
 * Positional Encoding: this is positional information because the self-attention's input does not have the positional information.  
 * Multi-Head attention: one of the self-attention methods.  
 * Add & Norm: residual connection and layer normalization.  
 * Feed Forward: Fully Connected layer.  
 ![Image of Yaktocat](https://github.com/ting-chih/NTU-ML2021spring/blob/main/image/encoder%20architecture.png)  
 
