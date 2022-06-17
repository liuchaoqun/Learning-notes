# Techniques to improve training speed
1. Set the dataloader properly. num_workers is recomended to be 4,8,16 and pin_memory is set to true. eg. 
```
{
  train_loader = DataLoader(train_dataset, batch_size=BS, num_workers=8, shuffle=True, pin_memory=True)
}
```
