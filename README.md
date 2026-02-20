# Florence Nightingale's Rose Diagram — A Replication

![Logo](assets/logo.png)

## The Story

During the Crimean War (1853-1856), Florence Nightingale collected data revealing that the majority of British military deaths resulted not from combat wounds but from preventable diseases caused by poor sanitary conditions. To communicate this sanitary reform crisis to policymakers, she created her iconic "coxcomb" or polar area diagram—a pioneering data visualization that made mortality patterns immediately apparent through proportional wedge areas. Her compelling visual argument directly influenced British military policy, leading to comprehensive hospital reforms and establishing data visualization as a powerful tool for driving evidence-based change.

## How the Data Was Collected

[Describe your digitization app and how you got coordinates → radii → areas.]

## The Math and Visualization

- Briefly explain that you used distances from the center to compute radii.
- Mention that areas are proportional to r².
- Note that each wedge encodes deaths from different causes.

## The Visualization

![Rose Diagram](output/nightingale_rose.png)

## Key Insights

- [Bullet about the left diagram (before reforms).]
- [Bullet about the right diagram (after reforms).]
- [Bullet about what this shows about data and policy change.]
- [Your own extra observation.]

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
