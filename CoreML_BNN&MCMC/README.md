<p> This is my solution for the Core ML question. It creates a BNN sampled with the Metropolis-Hastings Algorithm.
  The MLP has an input layer, a 2 neuron hidden layer and finaly the output layer. Each neuron has a signmoid activation. 
  I selected this model architecture as XOR problem has a non-linear seperation boundary. Also (A ⊕ B) = (AB)'.(A+B). The 2 neurons in the middle layer indicate the OR and the NAND.
  <br>
  <br>
  The weights are sampled by Metropolis Hasting algorithm with the proposal mean being the current mean of the weight and the proposal standard deviation as a hyperparameter.
  Also, the acceptance distibution is a uniform distribution which the difference in the current and new random variables must satisfy. The prior tries to implement the general ideology 
  of the neurons. Due to the randomness of the data, I did not include the normalization term as it was very close to 1 itself.
  <br>
  <br>
  I trained the model on 10,000 training data. 2000 iterations of the Hastings algorithm. The best model selected gave about 84.4% on a testing data of fresh 1000 samples. The weights of this model were saved. I also tried to ensemble the predictions of all the accepted models. This gave an accuracy of around 83%
  This is considerably better than the base line set by the random sampler which gave 55% best model accuracy and 51.7% ensemble accuracy when trained under similar circumstances!
  <br>
  <br>
 <p>
   
  
