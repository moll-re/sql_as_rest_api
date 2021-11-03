# sql_as_rest_api
Exposes a sql database as an api for stable sporadic r/w operations.
## The problem: 
When using a permanent sql connection but only sporadically writing to it, as in my telegram bot, the connection usually resets, resulting in an error.

I usually encounter `peewee.InterfaceError(0,"")` for which I can't find a solution for the life of me.

## The solution
Expose the database through a http server. Punctually connecting should be much more stable and the performance overhead should be negligible.
