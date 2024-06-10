# In summary
This software is designed to provide a hardware power cycling solution over a device running Home Assistant when Home Assistant becomes non-responsive for greater than 30 minutes.

**It has been written for and testing on**
a SONOFF S31 Lite power plug setup to control power to a Raspberry Pi running Home Assistant.

**License**
MIT

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the “Software”), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

 THE SOFTWARE IS PROVIDED “AS IS”, WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.

**Important note** 
There are always risks associated with turning off power to a device without an ordered shutdown having first being completed. These risks are present when using this software.  

# In more detail 
This software monitors Home Assistant and if Home Assistant becomes unresponsive to the device running this software for greater than 30 minutes then the device running this software powers off its relay and then powers it back on after 20 seconds - effectively power cycling the hardware on which Home Assistant is running.

**For this to work as intended** 
the device running Home Assistant must be plugged into the device running this software.  Also, the device running this software must have a Wi-Fi connection through to Home Assistant and be able to monitor that Home Assistant is running.

**If this software cannot access Wi-Fi** it will assume that Home Assistant is otherwise running just fine (this to prevent a power cycling of the device running Home Assistant simply because Wi-Fi is down).

**This software automatically turns on the relay of the device running this software** 
20 seconds after it has been turned off.

# Recommendation for first time use:

Ensure the device running this software has access to Home Assistant at the location it will be used before it is used to control power to the device running Home Assistant.

To do this is to plug the device running this software into to the power outlet that you intended to use with it, but do not yet plug anything into the device running this software.

Next, use ESPHOME's log feature to view the logs of the device running this software and confirm that you are seeing the messages 'Wi-Fi is connected' and 'Home Assistant is running' before plugging the device running Home Assistant into the device running this software.

# A helpful video 
on how to install ESPHome on a SONOFF S31 Lite can be found here:
https://www.youtube.com/watch?v=S4-HVYPCA2c

## Support

[<img alt="buy me  a coffee" width="200px" src="https://cdn.buymeacoffee.com/buttons/v2/default-blue.png" />](https://www.buymeacoffee.com/roblatour)
