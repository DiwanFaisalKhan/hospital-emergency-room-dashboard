# DAX Formulas Used in Hospital Emergency Room Dashboard

## Age Group Column
```DAX
Age Group = 
IF([Patient Age]>70, "70-79",
    IF([Patient Age]>60, "60-69",
        IF([Patient Age]>50, "50-59",
            IF([Patient Age]>40, "40-49",
                IF([Patient Age]>30, "30-39",
                    IF([Patient Age]>20, "20-29",
                        IF([Patient Age]>10, "10-19", "0-09")
                    )
                )
            )
        )
    )
)
```

## Patient Attend Status Column
```DAX
Patient Attend Status = IF([Patient Waittime]>30, "Delay", "Ontime")
```
