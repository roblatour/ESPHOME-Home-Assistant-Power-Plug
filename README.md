# In summary
This sketch is designed to provide a hardware power cycling solution over a device running Home Assistant when Home Assistant becomes non-responsive for greater than 30 minutes.

**It has been written for, and testing on**
a SONOFF S31 Lite power plug setup to control power to a Raspberry Pi running Home Assistant.

**IMPORTANT NOTE** 
THERE ARE ALWAYS RISKS ASSOCIATED WITH TURNING POWER OFF TO A DEVICE WITHOUT AN ORDERED SHUTDOWN HAVING FIRST BEEN COMPLETED. THESE RISKS ARE PRESENT WHEN USING THIS SKETCH.  USE IT AT YOUR OWN RISK.

# In more detail 
This sketch monitors Home Assistant and if Home Assistant becomes unresponsive to the device running this sketch for greater than 30 minutes then the device running this sketch powers off its relay and then powers it back on after 20 seconds - effectively power cycling the hardware on which Home Assistant is running.

**For this to work as intended** 
the device running Home Assistant must be plugged into the device running this sketch.  Also, the device running this sketch must have a Wi-Fi connection through to Home Assistant and be able to monitor that Home Assistant is running.

**If this sketch cannot access Wi-Fi** it will assume that Home Assistant is otherwise running just fine (this to prevent a power cycling of the device running Home Assistant simply because Wi-Fi is down).

**This sketch automatically turns on the relay of the device running this sketch** 
20 seconds after it has been turned off.

# Recommendation for first time use:

Ensure the device running this sketch has access to Home Assistant at the location it will be used before it is used to control power to the device running Home Assistant.

To do this is to plug the device running this sketch into to the power outlet that you intended to use with it, but do not yet plug anything into the device running this sketch.

Next, use ESPHOME's log feature to view the logs of the device running this sketch and confirm that you are seeing the messages 'Wi-Fi is connected' and 'Home Assistant is running' before plugging the device running Home Assistant into the device running this sketch.

# A helpful video 
on how to install ESPHome on a SONOFF S31 Lite can be found here:
https://www.youtube.com/watch?v=S4-HVYPCA2c
