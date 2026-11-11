Problem 1
Location: index 7. Problem: missing price. Evidence / command: df.isna().sum(). Proposed decision: flag. Reason: there is no value in it.

Problem 2
Location: index 19. Problem: price stated as 1,250. Evidence / command: inspect raw values, numeric conversion with comma removal. Proposed decision: retain the value as 1250 or flag it for review. Reason: the comma appears to be a thousands separator. Conversion changes representation, not the numeric amount. Because 1250 is far above most values, it should still be investigated.

Problem 3
Location: index 32. Problem: price of 9999. Evidence / command: describe(). Proposed decision: investigate, do not delete immediately. Reason: an extreme and unusual value but not necessarily an error.

Problem 4
Location: index 42. Problem: item labelled “oil b”. Evidence / command: df["item"].value_counts(). Proposed decision: investigate. Reason: it could be a typo or a casing error.

Problem 5
Location: index 98. Problem: exact duplicate of index 10. Evidence / command: df.duplicated(keep=False). Proposed decision: exclude one copy. Reason: keeping both would double the count of one.
