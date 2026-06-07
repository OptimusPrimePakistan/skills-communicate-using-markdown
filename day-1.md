# Daily Learning
## Morning Planning
- [ ] Finish Learn 2 Cloud
- [ ] P-rank P-2
- [ ] Finish this tutorial
## Review
` ` `bash
#!/bin/bash
echo "Welcome to the calculator!"

while true; do
    read -p "Enter a number: " a
    read -p "Enter another number: " b
    read -p "Enter your desired operation - (a)dd, (s)ubtract, (m)ultiplication, (d)ivision, (c)ounting from a to b: " c

    if [ "$c" = "a" ]; then
        echo $((a+b))
    elif [ "$c" = "s" ]; then
        echo $((a-b))
    elif [ "$c" = "m" ]; then
        echo $((a*b))
    elif [ "$c" = "d" ]; then
        if [ "$b" = "0" ]; then
            echo "Cannot divide by zero!"
        else
            echo $((a/b))
        fi
    elif [ "$c" = "c" ]; then
        for ((z=a; z<=b; z++)); do
            echo $z
        done
    else
        echo "You did not enter a correct operation."
    fi

    read -p "Do you want to restart? (y)es, or (n)o?: " i
    if [ "$i" = "y" ]; then
        continue
    fi
    if [ "$i" = "n" ]; then
        echo "Exitting....."
        break
    fi
done
` ` `
