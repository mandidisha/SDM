Benchmarking: Diversity & Novelty Comparison

1. Diversity
System: Content-Based
Dataset: Netflix
Diversity (ILD): 0.9932
Notes: Very high diversity; recommendations span a broad range of dissimilar movies.

System: Content-Based
Dataset: Yelp
Diversity (ILD): 0.0091
Notes: Extremely low; business features may cluster tightly (e.g., similar location or category).

System: SVD++
Dataset: Yelp
Diversity (ILD): 0.9998
Notes: Extremely high; nearly orthogonal rating vectors—maximum diversity in item recommendations.

System: SVD++
Dataset: Netflix
Diversity (ILD): 0.9904
Notes: Still very high; slightly lower than content-based, possibly due to latent structure constraints.

Interpretation:
Yelp's SVD++ recommender drastically improves diversity over its content-based version and achieves even higher values than Netflix. This shows that latent factor models (like SVD++) can uncover hidden item relationships and produce more varied recommendations.

2. Novelty
System: Content-Based
Dataset: Netflix
Novelty: 7.5733
Equivalent popularity: ~0.0052
Notes: Moderate novelty; recommended items are not extremely rare but not very common either.

System: Content-Based
Dataset: Yelp
Novelty: 14.5776
Equivalent popularity: ~0.00006
Notes: Extremely novel; the recommended items are very rare in the training data.

System: SVD++
Dataset: Yelp
Novelty: 14.3572
Equivalent popularity: ~0.00006
Notes: Almost identical novelty to content-based Yelp; recommends similarly rare items.

System: SVD++
Dataset: Netflix
Novelty: -5.0628
Notes: Negative value likely indicates an error in calculation; possibly due to taking log of a probability greater than 1.

Interpretation:
Yelp consistently provides higher novelty across both algorithms, suggesting that it often recommends very rare items. Netflix’s SVD++ output seems incorrect in this case and needs to be revisited. Among the valid results, Yelp SVD++ and content-based both suggest rare (novel) content.

Conclusion

Best Diversity: SVD++ on Yelp (0.9998)
Best Novelty: Yelp (both SVD++ and content-based, ~14.3+)
Most Balanced System: Netflix Content-Based (good balance of novelty and diversity without extremes)
Summary:
SVD++ significantly improves Yelp’s diversity, fixing the main limitation of its content-based recommender. Both approaches on Yelp maintain high novelty. Netflix content-based performs well in both novelty and diversity, offering a more balanced recommendation experience. Netflix SVD++ requires further debugging due to incorrect novelty output.