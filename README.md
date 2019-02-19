
<!-- README.md is generated from README.Rmd. Please edit that file -->
Diverging Graph Example
-----------------------

![](diverging.png)

``` r
data3 %>% 
  ggplot(aes(x = issue, 
             y = value, fill = barrier)) +
  geom_col() + 
  geom_label(data = data_totals, aes(x = issue, label = total), 
             fontface = "bold", show.legend = FALSE) +
  scale_fill_manual(
    values = c("darkorange3", "darkorange", "darkolivegreen", "darkolivegreen3", "white"), 
    breaks = c("Barrier Weak", "Barrier Strong", "Driver Strong", "Driver Weak")) +
  coord_flip()
```

See [make\_graph3.Rmd](make_graph3.Rmd) or make\_graph3.nb.html
