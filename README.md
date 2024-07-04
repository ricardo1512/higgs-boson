<p align="center" > <b> Universitat de Barcelona, Facultat de Matemàtiques i Informàtic </b> </p>

Posgraduate in Data Science and Machine Learning


Data Science in Particle Physics: The Higgs Boson


Capstone Project 2023/2024

Ricardo Vicente
______



Collisions in high-energy particle accelerators are crucial for discovering exotic particles and require Data Analysis approaches to solve 'signal' (1) versus 'background' (0) classification problems. 'Shallow' Machine Learning models have been limited in their ability to learn complex nonlinear functions, leading to a meticulous search for manually constructed nonlinear features.

Recent advances in the field of Deep Learning have allowed for learning more complex functions directly from the data, without the need for manually constructed features. Using benchmark datasets, Deep Learning methods have been shown to significantly improve classification metrics by up to 8% over the best current approaches.

While current approaches in high-energy physics have improved with manually constructed physics-inspired features, Deep Learning has proven to be more effective in automatically discovering powerful combinations of nonlinear features. Advances in Deep Learning, such as the use of neural networks with multiple hidden layers, have shown promise in improving the discrimination capability between signals and backgrounds in high-energy physics.

These developments in Deep Learning could inspire new advances in Data Analysis tools to address more complex problems in high-energy physics and could have applications in identifying decay products in high-dimensional raw detector data.
______

**1. Presentation of the chosen dataset**

The Higgs boson detection data has been produced using Monte Carlo simulations. The first 17 features (columns 1-17) represent kinematic properties measured by particle detectors in the accelerator (Low-Level). The last 7 features (columns 18-24) are functions of the first 17, designed by physicists to differentiate between the two classes (High-Level).

The variable set includes Low-Level features, which are direct measurements from particle detectors, and High-Level features, which are combinations of the former. These variables describe various aspects of particle collisions, ranging from the energy and momentum of individual particles to combined properties of multiple particles.
______

**2. General Features**

This dataset belongs to the "Classification in Numerical Features" benchmark. It is a smaller version (about 2.14%) of the original dataset, which contains 44 million rows. This version corrects the previous one in the definition of the class attribute, which is categorical, not numerical.

The author of this version is Daniel Whiteson from the University of California, Irvine, who selected 50% of experiments with ‘background’ and 50% with ‘signal’; it is, therefore, a balanced dataset.

Here is the link to the dataset: https://drive.google.com/file/d/1E6sGmKNBfVNg3uQVQAPCIU3HYqnp1hZC/view?usp=drive_link 
______

**3. Definition of the variables**

The variables are divided into 3 groups: kinematic or Low-Level, derived or High-Level, and the class label:

i. Kinematic or Low-Level features (numeric):

    lepton_pT (Lepton transverse momentum)
    lepton_eta (Lepton pseudorapidity)
    lepton_phi (Lepton azimuthal angle)
    missing_energy_magnitude (Missing energy magnitude)
    missing_energy_phi (Missing energy azimuthal angle)
    jet_1_pt (First jet transverse momentum)
    jet_1_eta (First jet pseudorapidity)
    jet_1_phi (First jet azimuthal angle)
    jet_2_pt (Second jet transverse momentum)
    jet_2_eta (Second jet pseudorapidity)
    jet_2_phi (Second jet azimuthal angle)
    jet_3_pt (Third jet transverse momentum)
    jet_3_eta (Third jet pseudorapidity)
    jet_3_phi (Third jet azimuthal angle)
    jet_4_pt (Fourth jet transverse momentum)
    jet_4_eta (Fourth jet pseudorapidity)
    jet_4_phi (Fourth jet azimuthal angle)

ii. Derived or High-Level features engineered by physicists (numeric):

    m_jj (Invariant mass of the dijet system)
    m_jjj (Invariant mass of the trijet system)
    m_lv (Invariant mass of the lepton-neutrino system)
    m_jlv (Invariant mass of the jet-lepton-neutrino system)
    m_bb (Invariant mass of the two b-tagged jets system)
    m_wbb (Invariant mass of the jet-lepton-neutrino and two b-tagged jets system)
    m_wwbb (Invariant mass of the jet-lepton-neutrino and four b-tagged jets system)

iii. Class label (categorical):

    label (Used to distinguish between signal [1] and background [0].)
______

**4. Presentation of the objectives**

This is a classification problem to distinguish between a signal process produced by Higgs bosons and a background process that does not.

The first objective of this work is to analyze the behavior of two types of models: one more 'superficial', such as the Extreme Gradient Boosting Classifier, and others of Deep Learning, such as the Multilayer Perceptrons, using the libraries Keras/Tensorflow and Scikit-learn.

The second objective concerns the variables. Which model better adapts to the Low/High-Level variables? With which types of variables do the models make better predictions? Will the models be capable of learning complex patterns in kinematic data to accurately classify observations into different categories (signal or background), without requiring manual intervention by physicists to create additional features?
______

**5. Project phases**

a. Frame the Problem

b. Get the Data

c. Visualize the Data

d. Prepare the Data

e. Select, Train and Fine-Tune the Models

f. Conclusions
______

**6. Reference**

Baldi, P. et al. Searching for exotic particles in high-energy physics with deep learning. Nat. Commun. 5:4308 doi: 10.1038/ncomms5308 (2014).

Baldi, P. et al. Enhanced Higgs to τ +τ − Search with Deep Learning. Physical Review Letters 114(11) doi: 10.1103/PhysRevLett.114.111801 (2014).
