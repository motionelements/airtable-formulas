
## Airtable formulas

### Past deadline / due date calculation

````
IF({deadline}=BLANK(),
    "",
	IF(AND({status}="on track", IS_BEFORE({deadline},NOW())),
        "⚠️ Past",
        "")
)
````
