---
sidebar_position: 1
title: Filter Object
---

import Thumbnail from '@site/src/components/Thumbnail';

## Filtering Data Objects in Your Action Flow

The `Filter Object` on-screen action in DronaHQ allows you to apply conditions to filter data from a data source provided that it should be in the form of an array of objects. This powerful feature enables you to select and display specific data based on your defined criteria.

<figure>
<Thumbnail src="/img/reference/actionflow-blocks/filter-object/filter-object.png" alt="Filter Object Window" />
<figcaption align='center'><i>Filter Object Window</i></figcaption>
</figure>



### Applying Filters

Here's how to use the Filter Object action:

1. Select the appropriate `data source` using a keyword that represents the array of objects you want to filter.

2. Provide a `filter condition` on that data source. This condition will determine which objects are included in the filtered result.

### Practical Application


Let's say our data source is `query_1`, which contains product information as key-value pairs. By applying a filter condition like `{{query_1.category == "Skincare"}}`, we can selectively work with entries that belong to a specific category. In this case, only the product(s) categorized under `“Skincare”` will be filtered and returned.

<figure>
<Thumbnail src="/img/reference/actionflow-blocks/filter-object/feild.png" alt="Filter Object Window" />
</figure>

### Versatile Filtering

The Filter Object action allows you to create more dynamic and responsive apps. You can filter data from various sources, including user input, external data feeds, or data stored in your app. By defining filter conditions, you can present users with tailored information that matches their preferences or requirements.


