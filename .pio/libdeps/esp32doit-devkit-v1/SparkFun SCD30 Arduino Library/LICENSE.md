SparkFun License Information

SparkFun SCD30 CO₂ Sensor
Die I²C-Adresse des Sensirion SCD30 Sensors ist standardmäßig 0x61. 
Es ist ein gängiger Wert für diesen Sensor, 
der für die Kommunikation mit Mikrocontrollern verwendet wird. 
Der SCD30 ist ein Sensor zur Messung von CO2, Temperatur und Luftfeuchtigkeit. 
Er verwendet die I²C-Schnittstelle für die Datenübertragung. 
Zusätzlich zur Standardadresse können Sie die Adresse ändern, indem Sie den SEL-Pin auf eine bestimmte Spannung ziehen, 
was die Verwendung mehrerer SCD30-Sensoren an einem einzigen I²C-Bus ermöglicht. 


Zwei I2C-Sensoren können problemlos parallel an einem Mikrocontroller betrieben werden, solange jeder Sensor eine eindeutige I2C-Adresse hat. Wenn die Sensoren die gleiche Adresse haben, wird ein I2C-Multiplexer benötigt, um die Kommunikation zu ermöglichen. 
Verständnis von I2C und Sensoren:

    I2C (Inter-Integrated Circuit):
    Ein serielles Kommunikationsprotokoll, das zwei Leitungen (SDA für Daten und SCL für Takt) verwendet, um mit mehreren Geräten (Sensoren, Displays, etc.) auf einem Bus zu kommunizieren. 

Sensoren:
Geräte, die physikalische oder chemische Größen (Temperatur, Druck, Licht, etc.) messen und diese Daten als elektrische Signale ausgeben. 
I2C-Adresse:
Jeder I2C-Sensor hat eine eindeutige Adresse, die vom Mikrocontroller verwendet wird, um mit ihm zu kommunizieren. 

Anschluss von zwei I2C-Sensoren:

    1. Eindeutige Adressen:
    Wenn die beiden Sensoren unterschiedliche Adressen haben, können sie direkt an die SDA- und SCL-Pins des Mikrocontrollers angeschlossen werden. Der Mikrocontroller kann dann gezielt mit jedem Sensor über seine Adresse kommunizieren. 

2. Gleiche Adresse:
Wenn die Sensoren die gleiche Adresse haben, wird ein I2C-Multiplexer benötigt. Der Multiplexer fungiert als Vermittler und erlaubt es, mehrere Geräte mit gleicher Adresse an einem einzigen I2C-Bus zu betreiben. Der Multiplexer schaltet dann jeweils einen Sensor zum Bus durch, sodass der Mikrocontroller mit jedem Sensor einzeln kommunizieren kann. 

Beispiel mit Arduino:
Ein Arduino kann problemlos mit zwei I2C-Sensoren umgehen. Wenn diese unterschiedliche Adressen haben, können sie direkt an die Pins A4 (SDA) und A5 (SCL) angeschlossen werden. Wenn sie die gleiche Adresse haben, kann ein I2C-Multiplexer zwischengeschaltet werden, um die Kommunikation zu ermöglichen. 
Zusätzliche Hinweise:

    Pull-Up-Widerstände:
    I2C-Busse benötigen in der Regel Pull-Up-Widerstände, um die SDA- und SCL-Leitungen auf einem hohen Pegel zu halten, wenn sie nicht aktiv sind. 

Geschwindigkeit:
I2C ist ein relativ langsames Protokoll, insbesondere im Vergleich zu SPI. Die übliche Geschwindigkeit liegt bei 100 kHz oder 400 kHz. 
Stromversorgung:
Achten Sie auf eine ausreichende Stromversorgung für alle angeschlossenen Geräte. 
Multiplexer:
Es gibt verschiedene I2C-Multiplexer, wie den TCA9548A von Texas Instruments, die es ermöglichen, mehrere Geräte mit gleicher Adresse an einem I2C-Bus zu betreiben. 


============================

SparkFun uses two different licenses for our files — one for hardware and one for code.

Hardware
---------

**SparkFun hardware is released under [Creative Commons Share-alike 4.0 International](http://creativecommons.org/licenses/by-sa/4.0/).**

Note: This is a human-readable summary of (and not a substitute for) the [license](http://creativecommons.org/licenses/by-sa/4.0/legalcode).

You are free to:

Share — copy and redistribute the material in any medium or format
Adapt — remix, transform, and build upon the material
for any purpose, even commercially.
The licensor cannot revoke these freedoms as long as you follow the license terms.
Under the following terms:

Attribution — You must give appropriate credit, provide a link to the license, and indicate if changes were made. You may do so in any reasonable manner, but not in any way that suggests the licensor endorses you or your use.
ShareAlike — If you remix, transform, or build upon the material, you must distribute your contributions under the same license as the original.
No additional restrictions — You may not apply legal terms or technological measures that legally restrict others from doing anything the license permits.
Notices:

You do not have to comply with the license for elements of the material in the public domain or where your use is permitted by an applicable exception or limitation.
No warranties are given. The license may not give you all of the permissions necessary for your intended use. For example, other rights such as publicity, privacy, or moral rights may limit how you use the material.


Code
--------

**SparkFun code, firmware, and software is released under the MIT License(http://opensource.org/licenses/MIT).**

The MIT License (MIT)

Copyright (c) 2020 SparkFun Electronics

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
