# PHTM
## PHTM is a PHP Date/Time Manipulation Library
### PHTM is a powerful PHP library for manipulating and formatting dates and times.

# Features
* Get and set the current timezone.
* Retrieve the current date/time in various formats.
* Format timestamps.
* Calculate the difference between two date/times.
* Modify a date/time by adding or subtracting intervals.
* Convert between 12-hour and 24-hour formats.
* Detect and convert date/time strings in various formats.
* Installation
* Simply include the PHTM class in your project:

# Usage
```
require_once 'PHTM.php';
```
# Usage Examples
## Set and Get Timezone
### Set the timezone to Asia/Dhaka
```
PHTM::setZone('Asia/Dhaka');
```
### Get the current timezone
```
echo PHTM::getZone(); // Output: Asia/Dhaka
```
### Get current date/time in default format (Y-m-d H:i:s)
```
echo PHTM::getTime(); // Output: 2024-06-27 12:34:56
```
### Get current date/time in custom format
```
echo PHTM::getTime('l, F j, Y g:i A'); // Output: Thursday, June 27, 2024 12:34 PM
```
### Format a Unix timestamp
```
echo PHTM::setTime(1672531199, 'Y-m-d H:i:s'); // Output: 2024-01-01 00:59:59
```
### Format a date/time string
```
echo PHTM::setTime('2024-06-27 12:34:56', 'd M Y, H:i'); // Output: 27 Jun 2024, 12:34
```
### Calculate the difference between two date/times
```
$diff = PHTM::calculate('2024-06-27 12:34:56', '2023-06-27 11:34:56');
print_r($diff);
/* Output:
Array
(
    [years] => 1
    [months] => 0
    [days] => 0
    [hours] => 1
    [minutes] => 0
    [seconds] => 0
)
*/
```
### Add 7 days to a date
```
echo PHTM::modify('2024-06-27 12:34:56', '+7 days'); // Output: 2024-07-04 12:34:56
```
### Subtract 1 year from a date
```
echo PHTM::modify('2024-06-27 12:34:56', '-1 year'); // Output: 2023-06-27 12:34:56
```
### Convert 24-hour to 12-hour format
```
echo PHTM::to12h('2024-06-27 14:34:56'); // Output: 2:34:56 PM
```
### Convert 12-hour to 24-hour format
```
echo PHTM::to24h('2024-06-27 2:34:56 PM'); // Output: 14:34:56
```
### Change format of a date/time string
```
echo PHTM::format('2024-06-27 14:34:56', 'd/m/Y H:i'); // Output: 27/06/2024 14:34
```
### Detect format of a date/time string and convert it
```
echo PHTM::format('June 27, 2024 14:34:56', 'Y-m-d H:i:s'); // Output: 2024-06-27 14:34:56
```
# Contributing
Contributions are welcome! Please feel free to submit a pull request or open an issue on GitHub.

# License
This project is licensed under the MIT License.
