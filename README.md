# Deep Graph Library

## Architecture
Show below, there are three sets of APIs for different models.
- `update_all`, `proppagate` are more global
- `update_by_edge`, `update_to` and `update_from` give finer control when updates are applied to a path, or a group of nodes
- `sendto` and `recvfrom` are the bottom primitives that update a message and node.

![Screenshot](graph-api.png)

## For Model developers
- Always choose the API at the *highest* possible level.
- Refer to [the default modules](examples/pytorch/util.py) to see how to register message and node update functions as well as readout functions; note how you can control sharing of parameters by adding a counter.

