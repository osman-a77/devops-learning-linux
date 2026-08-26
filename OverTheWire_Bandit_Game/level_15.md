# Level 14 → Level 15

## Challenge 
The password for the next level can be retrieved by submitting the password of the current level to port 30000 on localhost.

## Solution
```
cat /etc/bandit_pass/bandit14
echo "aaWecNkG4FhxJQxz07uiwzVP6bJiYS65" | nc localhost 30000
```

## Explanation
The password for the this level is stored in /etc/bandit_pass/bandit14 which can be read with the cat command. The password for the next
level can be retrieved by sending the current password to port 30000 on localhost via the nc command.

## Password
pbLYuZtTg4MgaqfJx8jbA9gKKGqM68A7

## What I learned
The nc command can be used to make network connections and receive/send raw data.
