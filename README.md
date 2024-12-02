![image](https://github.com/user-attachments/assets/40c31b3d-d3ae-4aa4-9122-e85bb6804bc6)# GenAI-Bootcamp-


## Prompt Engineering 
- The model takes in sequential text as an input and predicts what the token should be bsed on the data that it trained on.
- Promp engineering thus is teh process of designing the high quality prompts that guide LLMs to produce accurate outputs
- The goal is to provide output such as text summarization, information extraction , question and answering etc
  ##  LLM output configuration
  1. Output length
     - This is through selection of the number of tokens to generate in a  response. Generating more tokens leads to slower response times , higher energy and higher costs.
     - It is important in prompting techniques such as ReAct where teh LLM will keep emitting useless tokens after the response you want
       **  Sampling controls
          - LLms do not predict a single token. The llms predict what the next token could be . Those token probabilities are sampled to determine what the next produced token will be . Temp, top K , TOP P are the most common
      * Temparature
        - Controls the degree of randomnesss in token selection
        - Higher temparatures led to unpredictable and diverse results
        - Lower temparatures lead to a more deterministic response
        - A temparature of 0 (greedy decoding) is deterministic
          ![image](https://github.com/user-attachments/assets/ea07a847-ce1d-499f-8e18-b7763b75b8a6)
          this means that The model always chooses the token with the highest predicted probability at each step, leading to deterministic outputs.
However, if there’s a tie (two tokens have the same highest probability), the result may vary depending on how the tiebreaking is implemented.
      * Top K and top p
        - These are sampling techniques that are used in LLMs to restrict the predicted next token with the top predicted probabilities.
        - Top K - selects the top K most likely tokens from teh model's predicted distribution . The higher top K the more creative ad varies the output\. The lower the top K , the more restrictive and factual the model . The top K of 1 is equal to greedy decoding
        - Top P - selects the top tokens that have a cumulative probability does not exceeed a certain value of P . P values range from 0 to 1
        - ![image](https://github.com/user-attachments/assets/b69c7177-9c9b-4a91-bbf4-19989c716f5f)
-- If the temparature is 0, then the top k and top p will not be used. If the temparature is 9 (high) the tokens that fit in the precision either in the top p and top K are chosen at random.
![image](https://github.com/user-attachments/assets/58201cf7-c6d8-4e40-b752-649d471012e3)

![image](https://github.com/user-attachments/assets/4a5b254b-9b03-464b-9a85-dfc23e7cd3e5)
### Prompting Techniques
1. Zero shot
   - it provides a description of a task + text for the LLM to get started with
   - ![image](https://github.com/user-attachments/assets/e2ebe340-1fc3-4c98-88c4-1ce0a432eca5)
  2. One shot & few shot
     - One shot - provides a single example. The goal is to help it imitate the best complete the task
     - few shot - multiple example to increase the chances that the model follows the pattern. These is need to use thre to five examples 
     - 






          


