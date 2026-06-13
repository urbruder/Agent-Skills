# Formula Patterns

Use this reference for common spreadsheet formula families and platform differences.

## Lookup patterns

### Modern Excel lookup

```excel
=XLOOKUP(A2,LookupTable[ID],LookupTable[Result],"Not found")
```

### Google Sheets lookup

```excel
=XLOOKUP(A2,Lookup!A:A,Lookup!B:B,"Not found")
```

### Legacy compatible lookup

```excel
=INDEX(Lookup!B:B,MATCH(A2,Lookup!A:A,0))
```

### Two-way lookup

```excel
=INDEX(B2:E10,MATCH(H2,A2:A10,0),MATCH(H3,B1:E1,0))
```

## Conditional logic

### Basic IF

```excel
=IF(A2>=100,"Yes","No")
```

### Multiple conditions

```excel
=IF(AND(A2>=100,B2="Active"),"Qualified","Not qualified")
```

### Multiple outcomes

```excel
=IFS(A2>=90,"A",A2>=80,"B",A2>=70,"C",TRUE,"Needs review")
```

## Aggregation

### SUMIFS

```excel
=SUMIFS(Sales!D:D,Sales!A:A,A2,Sales!B:B,">="&DATE(2026,1,1))
```

### COUNTIFS

```excel
=COUNTIFS(A:A,"Active",B:B,">100")
```

### Average with criteria

```excel
=AVERAGEIFS(D:D,A:A,"Active",B:B,"North")
```

## Text formulas

### Extract text before a delimiter

Excel 365:

```excel
=TEXTBEFORE(A2,"-")
```

Compatible:

```excel
=LEFT(A2,FIND("-",A2)-1)
```

### Extract text after a delimiter

Excel 365:

```excel
=TEXTAFTER(A2,"-")
```

Compatible:

```excel
=RIGHT(A2,LEN(A2)-FIND("-",A2))
```

### Google Sheets regex extract

```excel
=REGEXEXTRACT(A2,"[0-9]+")
```

## Date formulas

### Days between dates

```excel
=B2-A2
```

### Days overdue

```excel
=MAX(0,TODAY()-A2)
```

### Month bucket

```excel
=TEXT(A2,"yyyy-mm")
```

### Quarter

```excel
="Q"&ROUNDUP(MONTH(A2)/3,0)
```

## Dynamic arrays

### Filter rows

Excel / Google Sheets:

```excel
=FILTER(A2:D100,B2:B100="Active")
```

### Unique sorted list

```excel
=SORT(UNIQUE(A2:A100))
```

## Google Sheets ARRAYFORMULA

```excel
=ARRAYFORMULA(IF(A2:A="","",A2:A*B2:B))
```

Use `ARRAYFORMULA` when the user wants a formula to fill an entire column automatically.

## Google Sheets QUERY

```excel
=QUERY(A1:D,"select A, sum(D) where B = 'Active' group by A label sum(D) 'Total'",1)
```

Use `QUERY` for SQL-like reporting in Google Sheets.

## Error handling

### Basic

```excel
=IFERROR([formula],"")
```

### Return message

```excel
=IFERROR([formula],"Not found")
```

Do not use `IFERROR` if hiding the error would make troubleshooting harder.

## Locale note

Some spreadsheet locales use semicolons instead of commas:

```excel
=IF(A2>0;"Yes";"No")
```

If the user reports separator errors, provide a semicolon version.

## Troubleshooting checklist

Check:

- wrong platform function
- missing quote
- missing parenthesis
- incorrect absolute reference
- using text numbers instead of numeric values
- date stored as text
- hidden spaces
- lookup value not exact
- mismatched range sizes
- array formula not supported
- sheet name needs single quotes
