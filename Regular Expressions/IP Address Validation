## Given an input of lines with at most one IP address per line, this
## algorithm can will print whether that line is a valid IPv4 or IPv6 address,
## or whether the line is neither

import re
import sys

regex1 = r"^(\d{1,3}\.){3}\d{1,3}$"
regex2 = r"^([a-f0-9]{1,4}:){7}[a-f0-9]{4}$"
regex3 = r"\d{1,3}"

lines = sys.stdin.readlines()

for line in lines:
    if re.search(regex1, line):
        good_num = True
        for num in re.finditer(regex3, line):
            if int(num.group()) > 255:
                good_num = False
        if good_num:    
            print "IPv4"
        else:
            print "Neither"
    elif re.search(regex2, line):
        print "IPv6"
    else:
        print "Neither"
