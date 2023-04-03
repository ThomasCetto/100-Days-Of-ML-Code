# Backpropagation

[3B1B video](https://www.youtube.com/watch?v=Ilg3gGewQ5U&list=PLZHQObOWTQDNU6R1_67000Dx_ZCJB-3pi&index=3)

It is a technique used to adjust the weights of the connections between neurons in order to improve the accuracy of predictions.

It works by propagating the error from the output layer back through the layers, adjusting the weights at each layer so that the error is minimized.

It starts by comparing the predicted output to the actual output, and then calculates the difference between them (the error).

Then, it goes backwards through the layers, calculating how much each neuron contributed to the final output, and then adjusts the weights of the connections between the neurons accoridingly, in order to reduce the overall error.

This process is repeated multiple times, with each iteration of backpropagation helping to fine-tune the weights and improve the accuracy of the predictions.