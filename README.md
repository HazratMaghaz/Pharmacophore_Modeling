# Pharmacophore_Modeling
Pharmacophore_Modeling step by step Guide through MOE.

- Merge activity values:
- Open **DBV > File > Merge...**
- Merge the packed database with the original database (used as Database 2).
- Ensure *New Database* is deactivated.

---

## 🧪 Step 2: Building the Pharmacophore Model

- Use an active compound from the original database as a template.
- Hide hydrogens using **MOE > Render > Hide > Hydrogens**.
- Open **Pharmacophore Query Editor**:
- File > New > Pharmacophore Query...
- Change Ligand Annotation to *Long* for feature labels.
- **Create Features**:
- Select annotation points and create features.
- Adjust feature radius and rendering as needed.
- **Search Settings**:
- Load the packed conformational database.
- Set *Hit Entries: Select* and *Results: No Output*.
- Run the search to identify matching conformers.

### 🛠 Troubleshooting Feature Matching

- **Too few hits**:
- Increase feature radius
- Reduce number of features (use *Ignore* or *Enable Partial Match*)
- **Too many hits**:
- Decrease radius
- Add more selective features

---

## 📊 Step 3: Model Comparison

- In **Pharmacophore Search**, set *Results: Conformations* and configure *Code* and *EC50*.
- Sort conformations using **DBV > Compute > Sort**:
- Priority 1: mseq, Priority 2: rmsd
- Select best entries:
- Use *Select Unique Entries* based on *Code* or *mseq*
- Hide unselected entries
- Visualize top conformations in the MOE viewer.

---

## 🔎 Step 4: Predicting hERG Liability

- Use the final pharmacophore model to screen unknown compounds.
- Record model input:
- Template compound
- Features used and their distances (via **MOE > Edit > Measure > Distances**)
- Evaluate model's ability to distinguish active vs inactive compounds
- Compare predictions for structurally similar compounds

---

## 🧾 Outputs

- Pharmacophore model file (.ph4)
- Visualizations: feature maps, conformations
- Summary table with model performance and selected features
- Prediction results on unknown dataset

---

## Tools Used

- MOE (Molecular Operating Environment)
- Data files: training, validation, and unknown compound sets
"""

