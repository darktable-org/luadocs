---
title: image_time
id: image_time
weight: 190
draft: false
author: "people"
---

## Name

image_time.lua - synchronize image time for images shot with different cameras

## Description

image_time non destructively adjusts image times by modifying the 
database image exif_datetime_taken field.  There are 4 modes: adjust time,
set time, synchronize time, and reset time.

### ADJUST TIME

adjust time mode lets you chose an offset in terms of years, months,
days, hours, minutes, and seconds.  The adjustment can be added or
subtracted.  

WARNING:  When adding and subtracting months the result will usually
be what is expected unless the time being adjusted is at the end of 
the month.  This is because a month is a variable amount of time that
can be 28, 29, 30 or 31 days depending on the month.  Example: It's 
March 31st and I subtract a month which not sets the time to February
31st.  When that gets set to a valid time, then the date changes to
March 3rd.

### SET TIME

set time mode allows you to pick a date and time and set the image
time accordingly.  Fields may be left out.  This is useful when 
importing scanned images that don't have an embedded date.  

### SYNCHRONIZE TIME

I recently purchased a 7DmkII to replace my aging 7D.  My 7D was still
serviceable, so I bought a remote control and figured I'd try shooting
events from 2 different perspectives.  I didn't think to synchonize the 
time between the 2 cameras, so when I loaded the images and sorted by
time it was a disaster.  I hacked a script together with hard coded values
to adjust the exif_datetime_taken value in the database for the 7D images 
so that everything sorted properly.  I've tried shooting with 2 cameras 
several times since that first attempt.  I've gotten better at getting the
camera times close, but still haven't managed to get them to sync.  So I
decided to think the problem through and write a proper script to take 
care of the problem.

### RESET TIME

Select the images and click reset.  

## Usage

### ADJUST TIME

Change the year, month, day, hour, minute, second dropdowns to the amount
of change desired.  Select add or subtract.  Select the images.  Click 
adjust.

### SET TIME

Set the time fields to the desired time.  Select the images to change.  Click
set.

### SYNCHRONIZE TIME

Select 2 images, one from each camera, of the same moment in time.  Click
the Calculate button to calculate the time difference.  The difference is
displayed in the difference entry.  You can manually adjust it by changing
the value if necessary.

Select the images that need their time adjusted.  Determine which way to adjust
adjust the time (add or subtract) and select the appropriate choice.

If the image times get messed up and you just want to start over, select reset time
from the mode and reset the image times.

### RESET TIME

Select the images and click reset.

## Additional Software Required

* exiv2

## Limitations


## Author

Bill Ferguson - wpferguson@gmail.com

