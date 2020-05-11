[Original video](https://www.youtube.com/watch?v=TWwvJw6UoxY)

/dev/null is a bit bucket, it will disgard everything that is being written into it, but it will return success in write.

`cat *.pgn > /dev/null`

`cat *.pgn | grep "Result"`

`cat *.pgn | grep "Result" | sort | uniq -c`

`sleep 3 | sleep 5 | echo '8'` -> executed in parallel, 8 will be printed immediately, but the command will end in 5s.

