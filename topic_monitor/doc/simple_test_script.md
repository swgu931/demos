1) Comparing reliability QoS settings

```
ros2 launch topic_monitor reliability_demo.launch.py (@server)
ros2 run topic_monitor topic_monitor --display --allowed-latency 5 (@client)
```
------

2) Comparing the latency of reliability QoS settings
```
ros2 run topic_monitor topic_monitor --display --allowed-latency 1 (@client)
```
----------------

2) Comparing the effect of queue depth
```
ros2 launch topic_monitor depth_demo.launch.py (@server)
ros2 run topic_monitor topic_monitor --display (@client)
ros2 run topic_monitor topic_monitor --display --allowed-latency 1 (@client)
```

------------------

3) Comparing the effect of data size

```
ros2 launch topic_monitor fragmentation_demo.launch.py (@server)
ros2 run topic_monitor topic_monitor --display --expected-period 4 (@client)
```
----------------------