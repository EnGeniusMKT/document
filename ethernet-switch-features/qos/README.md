# QoS

Quality of Service \(QoS\) allows implement priority queuing within a network. QoS is a means of providing consistent and predictable data delivery to the switch by distinguishing between packets that have stricter timing requirements from those that are more tolerant of delays. QoS enables traffic to be prioritized while avoiding excessive broadcast and multicast traffic. Traffic such as Voice and Video streaming which require minimal delays can be assigned to a high priority queue, while other traffic can be assigned to a lower priority queue, resulting in uninterrupted actions. Without QoS, all traffic data is as likely to be dropped when the network is congested. This can result in reductions in network performance and hinder the network in time-critical situations. 

In a switch, multiple queues per port are often provided to give preference to certain packets over others based on user-defined criteria. When a packet is queued for transmission within a port, the rate at which it is processed depends on how the queue is configured and the amount of traffic present within other queues on the port. If a delay is necessary, packets are held in the queue until they are authorized for transmission.  
  
****

