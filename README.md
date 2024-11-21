# timecalc

Just add and subtract time.

For now it's only `A + B` and `A - B` expressions (whitespace ignored).  
All `A` or `A+B+C+...` would not be parsed.

```
>>> 8:30 + 9:15:18
 17 h 45 m 18 s
>>> 8:20+8:30
 16 h 50 m 
>>> 14:00 + 25:00:03
1 d 15 h  3 s
>>> 12: - 1:10
 10 h 50 m 
>>> :14:1 + ::47
  14 m 48 s
>>> 
```

You can omit values (except at least one) and one right colon ':'. 
Implicit HH:MM. So `:2` is two minutes and `::3` is three seconds.

You can insert small number or huge number — they would be parsed until they are near colons.

```
>>> 11:30 + :198
 14 h 48 m 
```
