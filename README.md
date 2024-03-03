# calc ( calculator with bash scripting ) 
#!/bin/bash

echo -e "please enter you number :\c"
read num1
echo -e "now please enter your second number : \c"
read num2

echo -e "now you have to enter you oparater : \c"

read char1

case $char1 in
          + )
                  result=$(( num1 + $num2  )) ;;
          - )
                 result=$(( num1 - $num2  )) ;;
          / )
                  result=$(echo "scale=2; $num1 / $num2" | bc ) ;;
          * )
                 result=$(( num1 * num2 )) ;;
esac
echo "bro answer is $result"
