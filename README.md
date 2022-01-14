# Recommendation_system_network_database

## Data source: http://jmcauley.ucsd.edu/data/amazon/links.html
- subset: Sports and Outdoors (Metadata, reviews)

## methodology

1. Build graph database with df_meta.related
- {'bought_together' : 1, 'also_bought' : 2, 'also_viewed' : 3}
3. Update edges weight with customer reviews
- Initial alpha = 0.5
- score = (overall * alpha) + (helpful * (1-alpha))
