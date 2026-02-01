# Whisplay-driver_for_pwnagotchi
This contains the whisplay driver and wrapper for the Pwnagotchi specifically Jayofelony's fork 

Add the following to /home/pi/.pwn/lib/python3.11/site-packages/pwnagotchi/utils.py


elif config['ui']['display']['type'] in ('whisplay'):
        config['ui']['display']['type'] = 'whisplay'
_________________________________________________________________________


Add the following to /home/pi/.pwn/lib/python3.11/site-packages/pwnagotchi/ui/display.py

def is_whisplay(self):
        return self._implementation.name == 'whisplay'
_________________________________________________________________________

Add the following to /home/pi/.pwn/lib/python3.11/site-packages/pwnagotchi/ui/hw/__init__.py 


elif config['ui']['display']['type'] == 'whisplay':
        from pwnagotchi.ui.hw.whisplay import Whisplay
        return Whisplay(config)
_________________________________________________________________________
————————————————————————————————————————--

Place the whisplay.py file in directory /home/pi/.pwn/lib/python3.11/site-packages/pwnagotchi/ui/hw/

—————————————————————————————————————————

Place folder /whisplay in the directory /home/pi/.pwn/lib/python3.11/site-packages/pwnagotchi/ui/hw/libs 
