# Using a HID ProxPro Proximity Reader 

* Part number 5355AGN00 or 5355-300-01 or 2905-000936 or "Part No. 70-00859"
* Refers to operators manual 5355A-900 REV N.x (for example, [here](https://www.hidglobal.com/doclib/files/resource_files/5355a-900-n.3-proxpro-wiegnad-clock-and-data-install-guide-en.pdf)).

The manual says that 5355AGN00 means:

* 5355 = Model Number 5355 = ProxPro Wiegand (not ProxPro Clock/Data)
* A = Model Number Suffix
* G = Color - G = Gray, B = Beige
* N = Standard Hardware Options - N = None (no keypad, which are options K, S, and D)
* 00 = Configuration Options - (00 standard)

Unclear what 5355-300-01 means besides the cryptic phrase "Final Assembly Number = 5355-300-XX Changes with Revisions"

## Connections

| TB1 | Label                    | Notes |
|-----|--------------------------|-------|
|  01 | DC+(RED)                 | Back label claims 10 - 28.5 Vdc at 155 mA. Manual claims "DC Power Supply 12V/100mA or 24V/120mA" |
|  02 | GROUND (BLACK)           | Yep, Ground |
|  03 | DATA 0/DATA (GREEN)      |
|  04 | Data 1/CLOCK (WHITE)     |
|  05 | RETURN(VIOLET)           | Manual says "Shield Ground" so this can probably be ignored if you have a common ground. |
|  06 | GREN LED (ORANGE)        |
|  07 | RED LED (BROWN)          |
|  08 | BEEPER (YELLOW)          |
|  09 | HOLD/CARD PRESENT (BLUE) | 
|  10 | TAMPER COMMON            |
|  11 | TAMPER SELECT            |

## DIP Switch 1

| # | Name                    | Notes |
|---|-------------------------|-------|
| 1 | Hardware Identity       | Let's use Wiegand: ON |
| 2 | Audible Tone Control    | We want the auto beepy: ON |
| 3 | Green LED Control       | We want the green to flash when reading: OFF |
| 4 | Keypad Operation        | N/A, so leave default: ON |
| 5 | Single/Dual LED Control | LED usually red: OFF |
| 6 | Wiegand Data 1 Bias     | Pulled up to +5V through 1Kohm: ON |
| 7 | Wiegand Data 0 Bias     | Pulled up to +5V through 1Kohm: ON |
| 8 | Not used                | Default: ON |

... which is what the switch was already set to, and seems to be the default as shown in the manual and on the printout sheet in the reader.


