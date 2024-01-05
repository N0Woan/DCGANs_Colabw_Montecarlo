# DCGANs
- GANs is basically a framework where we simultaneously train two models include a generator (use to simulate the data distribution) and a discriminator (use to distinguish a sample is from the data distribution or the generator). This can be consider as a minimax game, where we train D (discriminator) to maximize the probability of assigning the correct label to both training examples and samples from G (generator) and we simultaneously train G to minimize $log(1-D(G(z)))$ (z is a random noise):

 $$\min G \max D V(D, G)=\mathbb{E}{\boldsymbol{x} \sim p{\text {data }}(\boldsymbol{x})}[\log D(\boldsymbol{x})]+\mathbb{E}{\boldsymbol{z} \sim p{\boldsymbol{z}}(\boldsymbol{z})}[\log (1-D(G(\boldsymbol{z})))]$$

- DCGANs have the basic like GANs but there are some additions features, that they use 2 main layers are convolutional layer and transposed convolutional layer.
- Our goal is to find how to implement this in code with pytorch and CIFAR10 data set.
