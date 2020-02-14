
## Airtable formulas

### Get day of week

Get `Mon`, `Tue`, `Wed`...

`IF({Deadline}, DATETIME_FORMAT({Deadline}, 'ddd'))`


### Past deadline / due date calculation

````
IF({Deadline}=BLANK(),
    "",
	IF(AND({Status}="on track", IS_BEFORE({Deadline},NOW())),
        "⚠️ Past",
        "")
)
````
