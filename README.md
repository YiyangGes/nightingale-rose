<!-- # Florence Nightingale's Rose Diagram — A Replication

![Logo](assets/logo.png) -->

<p align="center">
  <img src="assets/logo.png" width="150"/>
</p>

<h1 align="center">Florence Nightingale's Rose Diagram — A Replication</h1>

## The Story

During the Crimean War (1853-1856), Florence Nightingale collected data revealing that the majority of British military deaths resulted not from combat wounds but from preventable diseases caused by poor sanitary conditions. To communicate this sanitary reform crisis to policymakers, she created her iconic "coxcomb" or polar area diagram—a pioneering data visualization that made mortality patterns immediately apparent through proportional wedge areas. Her compelling visual argument directly influenced British military policy, leading to comprehensive hospital reforms and establishing data visualization as a powerful tool for driving evidence-based change.

![Nightingale's Diagram](assets/3815a Large.jpg){#fig-rose}

## How the Data Was Collected

Since their is no exact count of mortality, we need to get the wedge areas by ourself. Here is how to do it.

(@) Take out individual wedge areas
    * Open the original diagram (@fig-rose) using some painting applications (I am using Krita), and trace outline of wedges.
    * Use a photo editor to make the wedges area transparent, then save each wedge area as a PNG file with alpha (or transperancy) channel.
    * Save all wedges area with name yyyy-mm_(Cause of death).png to one folder.

![An example of transperant wedge area](assets/image.png){width=30%}

(@) Count the pixel that is transperant from PNGs to get the pixel number of each wedges using Python. Save the pixel number to csv for later processing.

## The Math and Visualization

- With area being pixel count, the propotion of the radii can be represent
by the square root of the area. Therefore, the radii can be calculated by getting the square roots of pixel counts of each categories.

```python
radii_other = np.sqrt(df['other'])
radii_wound = np.sqrt(df['wound'])
radii_disease = np.sqrt(df['disease'])
```

## The Visualization

<!-- ![Rose Diagram](output/nightingale_rose.png) -->

::: {#fig-recreations layout-ncol=2}

![1854-1855](output/recreation.png){#plt-recreation1}

![1855-1856](output/recreation2.png){#plt-recreation2}

Recreation of Nightingale's Rose diagram 
:::

## Key Insights

- [Bullet about the left diagram (before reforms).]
- [Bullet about the right diagram (after reforms).]
- [Bullet about what this shows about data and policy change.]
- The plot shows the great contrast of the propotion between the blue area (disease), and the red area (wounds). The contrast make it convincing that sanitation is indeed a significant factor in mortality counts. There might be limitation for polar chart too. Firstly, it would be hard to show to overall trend of the data. Secondly, for 2 similar counts, it would be hard to tell the difference because human is not sensitive to area. The limitations would be compensate by some alternative visualization ways.

## Technical Details

- Language: Python  
- Libraries: [list your main libraries]  
- Files:
  - `src/digitize_app.py`  
  - `src/plot_rose.py`  
  - `data/coordinates.json`  
  - `data/nightingale_computed.csv`  

## How to Run

1. Clone this repository.  
2. Create and activate a virtual environment (optional).  
3. Install requirements (if you have a `requirements.txt`).  
4. Run the plotting script:  
   `python src/plot_rose.py`  

## What I Learned

[2–3 sentences written entirely by you: technical lessons and reflections.]

## References

- [Short list of sources or links you used.]
