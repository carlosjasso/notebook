# Windows DOS - Get Time in UTC

Script:

```bat
@echo off
Setlocal EnableDelayedExpansion
call :get_utc_time

:: Add leading zeros
Set gmt_minute=0%gmt_minute%
Set gmt_minute=%gmt_minute:~-2%
Set gmt_day=0%gmt_day%
Set gmt_day=%gmt_day:~-2%
Set gmt_month=0%gmt_month%
Set gmt_month=%gmt_month:~-2%

:: Display result
Echo %USERNAME%,%gmt_year%-%gmt_month%-%gmt_day% %gmt_hour%:%gmt_minute%:%gmt_second%
pause
goto :eof

:get_utc_time
for /f "tokens=1,2 delims==" %%G in ('wmic path Win32_UTCTime get /value ^| find "="') do (call :setUTCvars %%G %%H)
goto :eof

:setUTCvars
   Set _var=%1
   Set _value=%2
   Set gmt_!_var!=!_value!
goto :eof
```
