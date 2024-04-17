# llms
Document understading of LLMs


## Transfomers paper

- [x] Implement the transformer paper - (ref: https://www.youtube.com/watch?v=kCc8FmEb1nY&t=2215s)
    Tasks
    - [x] Implement Bigram Model
    - [x] Implement self attention logic in adhoc fashion
    - [x] Implement self attention logic as part of the Bigram model
    - [x] Implement a single multi head attention block as part of bigram model
    - [x] Implement multiple layers of multi head attention block as part of bigram model
        - [x] add feed forward NN
        - [x] add residual connection
        - [x] add layer norm
    - [ ] Check this implementation with implementation [by Karparthy Sab](!https://github.com/karpathy/ng-video-lecture)
    - [ ] List the differences and next steps to think about here.
        - [ ] dropout layers need to be included
        - [ ] linear layer missing in multihead attention class
        - [ ] length of linear layer in multihead attention class needs to scaled up (4 x head_size)
        - [ ] projection layer needs to be added to bring 4 x head_size to head_size
        - [ ] add dropout at the last of multuheadattention layer
        - [ ] feedforward in block with two linear layers, emb -> 4*emb -> emb (sacle up and bring back)
        - [ ] dropout inside this feedforward network
        - [ ] use multiheadattention in block instead of nn module list (easy refactor)
        - [ ] 




## Previous work

- [ ] Read through the coursera genai course finsihed materials.

- [ ] Get an overview for the current status



