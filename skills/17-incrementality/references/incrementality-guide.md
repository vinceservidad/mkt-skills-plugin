# Incrementality guide

## Methods

| Method | Use when | Watch for |
| --- | --- | --- |
| User holdout | The platform supports a conversion lift study | Platform rules and minimums change; cite current docs |
| Geo-lift | You can turn spend on and off by region | Regions must be matched on past sales; spillover |
| Time on/off | Nothing else possible | Seasonality and other changes confound |

## Groups

Pick regions before launch, matched on past weekly sales and trend. Keep other changes out of both.

## Size

Detectable effect depends on baseline volume and week-to-week variation. With small volume, a test may need more weeks or bigger regions; if it still can't detect the effect that matters, change the question.

## Read

Lift = (test − control, scaled to the same baseline). Incremental CAC = test spend ÷ incremental customers. Report uncertainty and scope.
