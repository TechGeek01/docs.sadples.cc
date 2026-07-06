# Fixing Alarms
## Sekure Controls SK-800ME
### Setting the PIN

!!! note
	The default PIN is `1234`. I will assume this default PIN in this guide.

1. Disarm the alarm with the current PIN (ex. `1234`)
2. Enter programming mode

	`# [current PIN] *`

	The yellow `Keypad Program` LED will turn on

3. Enter the new code, and exit programming mode

	`6789 & #`

	The yellow `Keypad Program` LED will turn off

!!! warning
	The alarm will reset to the default PIN every time power is completely lost. If it's not running on either battery or AC power, the PIN will reset.

	Yes, that means that if you've unplugged it while changing the batteries, your PIN that you had set is not set anymore, and you will need to use the default `1234`.
