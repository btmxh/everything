[[data]] put in [[computer]] must be [[encode]]d into [[binary]] numbers (binarization)
data types
- human made: according to standards made by human
- natural data: physical signals: image, audio, etc.
rules:
- human made
	- number -> using standards
	- characters -> using text encoding standards, character sets, etc.
- natural data:
	- must be digitization before importing to [[computer]]
	- analog signal --(sensor)---> ces  --(adc)-->digital signal -> [[computer]]
	- analog signal <-(recreator)- ces <--(dac)-- digital signal <- [[computer]]
		- adc: analog -> digital converter
		- dac: digital -> analog converter
		- ces: continuous electrical signal

## basic data
- int
	- [[unsigned]]: binary
	- [[signed]]: 2's complement
- real
	- fixed
	- float
- char
	- encodings: utf-8, utf-16, etc.
- length usually divides by 8

## structured
uses basic data types
e.g. array, string, set, records, etc.