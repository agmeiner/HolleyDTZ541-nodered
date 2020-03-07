# HolleyDTZ541-nodered

Read data from two Holley DTZ 541 energymeter with Node-RED and push it to a database. 
There are two Holley energymeter of the same type.

## Used nodes
 - node-red-contrib-simpletime: generate a timestamp for the values. (version 2.8.1)
 - node-red-contrib-smartmeter: to read out the data comfortably from the energymeter (version 0.2.3)
 - node-red-node-mysql: to access a mysql database (version 0.0.19)

## Energymeters

### holley-pv 
 The first counts 
  - in 1.8.0 the consumed energy of the pv-system,
  - in 2.8.0 the generated energy of the pv-system. The energy can be consumed by the house or delivered to the power grid. 

### holley-net
The second counts
  * in 1.8.0 the received energy from the power grid. This is the case, when there is not enough energy from the pv-system. 
  * in 2.8.0 the delivered energy to the power grid. This is the case, when there is more energy from the pv-system than the house consumes. 
  

Thanks to [hacki11](https://github.com/hacki11) for providing a workaround for Holley DTZ 541 in the used smartmeter libraries.
