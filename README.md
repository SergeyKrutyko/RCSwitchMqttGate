# RCSwitchMqttGate
Remote Control of Livolo Switch &amp; Other 433Mhz Devices to MQTT

Данный скрипт написан для чтения кодов сигналов от устройств и пультов по радиоканалу 433Мгц и отправки их на MQTT сервер, где можно их перехватывать умным домом. 

В обратку реализовано включение выключение радиовыключателей света LIVOLO. Чтобы гарантировано включать или выключать, используются сцены. Т.е. выключатель программируется на первую сцену включенным. А на вторую как выключеный. Таким образом удалось избежать переключения, как с пульта. А именно включение или выключение. Управление идет также по MQTT. Выставляется TOPIC livolo/switch(1..9) и сообщение в него 0 или 1. Для обучения выключателей необходимо перевести его в режим обучения и после сигнала выбрать состояние включен или выключен. Соответственно на состояние включен - посылаем комманду 1 и обучаем его включаться. А на состояние выключен - посылаем комманду 0 и обучаем выключаться.


This script is written to read the codes of signals from devices and consoles via radio channel 433 MHz and send them to the MQTT server, where they can be intercepted by a smart house.

In turn, the switching-off of LIVOLO radio switches is realized. To ensure turn on or off, scenes are used. Those. The switch is programmed to the first stage on. And the second as off. Thus, it was possible to avoid switching, as from the console. Namely, switching on or off. Management is also on MQTT. The TOPIC livolo / switch (1..9) is displayed and the message 0 or 1 is displayed. To learn the switches, it is necessary to put it into the training mode and after the signal select the state is on or off. Accordingly, the state is on - send command 1 and train it to turn on. And the state is off - send command 0 and learn to turn off.
