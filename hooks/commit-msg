#!/bin/sh
shopt -s nocasematch  # Case insensitive matching
shopt -s extglob

RED='\033[0;31m'
regex='^(fix(es)?|change(s)?|merge(s)?|update(s)?|add(s)?remove(s)?)[[:space:]].+[a-zA-Z?!${}()@].{5,}'

# Get commit Message
#file=`cat $1` 

# Test commit message conforms to regex requirements. 
if ! [[ $1 =~ $regex ]]; then
    echo "${RED} Commit messages must be prefixed with singular or plural fix, change, merge, add. \n Example 'Adds new API connection input to dash' and at least 5 characters long"    
    exit 1; 
    else 
    echo "Success"  
fi
