# Level 14 → Level 15

## Challenge 
The password for the next level can be retrieved by submitting the password of the current level to port 30000 on localhost.

## Solution
```
cat /etc/bandit_pass/bandit14
echo "aaWecNkG4FhxJQxz07uiwzVP6bJiYS65" | nc localhost 30000
```
