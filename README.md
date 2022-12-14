# Parking Space Detection

Finding parking space for your vehicle is a major problem in big cities. The rise of car ownership has created an imbalance between parking demand and supply. In the current situation, a parking management system that can track parking spots has become a necessity for all major cities. The system has to be scalable, efficient, reliable, and affordable at the same time. In recent years, the advances in deep learning powered computer vision algorithms have shown very promising results in a variety of tasks. Similar techniques can be used to address the problem of parking space detection.

Requirements:
torch==0.4.1
torchvision==0.2.1
matplotlib==3.2.2


### Download dataset
There are 3 sets of dataset and their labels required to run this code. Run [get_dataset.sh](get_dataset.sh) as follows:

```
bash get_dataset.sh
```

This command will download the datasets and unzip them in the project root directory.
Make sure to include the correct directory in the next section when parsing the argument.


### Running the code
Run the code as follows:

```
python3 main.py
```

By default, it runs `epochs=18`, train on `CNRPark Even` and test on `CNRPark Odd`. 
If a trained model is to be loaded and test on other dataset (i.e. `.pth` file exists), or AlexNet is to be used, run the following command:

```
python3 main.py --path trained_model/sunny.pth --model AlexNet
```

See arguments in [options.py](utils/option.py).

### Requirements
```
python >= 3.6
pytorch >= 0.4
```

### References
```
@article{amato2017deep,
  title={Deep learning for decentralized parking lot occupancy detection},
  author={Amato, Giuseppe and Carrara, Fabio and Falchi, Fabrizio and Gennaro, Claudio and Meghini, Carlo and Vairo, Claudio},
  journal={Expert Systems with Applications},
  volume={72},
  pages={327--334},
  year={2017},
  publisher={Pergamon}
}
```
