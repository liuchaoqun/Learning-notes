# Techniques to improve training speed
1. Set the dataloader properly. num_workers is recomended to be 4,8,16 and pin_memory is set to true. eg. 
> train_loader = DataLoader(train_dataset, batch_size=BS, num_workers=8, shuffle=True, pin_memory=True)
> More details can be found here: https://blog.csdn.net/qq_32998593/article/details/92849585
2. Train with multiple GPUs
3. When training a transformer-like model, the max_length of tokens is quite important. Try to set the max_length to a smaller value based on the characteristic of sentences.
4. Use [automatic mixed precision](https://pytorch.org/tutorials/recipes/recipes/amp_recipe.html).
