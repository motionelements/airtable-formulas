
## Airtable formulas

### Past deadline / due date calculation

````
IF({Deadline}=BLANK(),
    "",
	IF(AND({Status}="on track", IS_BEFORE({Deadline},NOW())),
        "⚠️ Past",
        "")
)
````
