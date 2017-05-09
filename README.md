
This is an Ethics-Driven Design guideline for parties involved in the research and development of **XXX**, one of the most advanced Autonomous Unmanned Aerial Vehicle (AUAV) systems dedicated entirely to humanitarian courses. In other words, designers, engineers, social scientists, ethics consultants and marketers of the project should use this guideline as a constant reference while advancing the design, the capabilities, and the promotional strategies for the system.

This guideline is originally drafted by the CVO (Chief Values Officer) of the company. However, ethical responsibility should not be delegated to chief values officers alone, and it is the obligation of all members of the company to act ethically responsibly throughout the design, development, and marketing process.

It is highly encouraged that all members of the company use this repository as the platform to keep an ongoing discussion and contribute contents in the form of pull requests.

# 1. Technical roundup

### Types of drone AIs currently in production
List of the latest autonomous drone systems currently in production by our company, categorized by its intended purposes.

* Crisis Response **XXX**
  * [Crisis Mapping](https://en.wikipedia.org/wiki/Crisis_mapping)
  * [Search and Rescue](https://en.wikipedia.org/wiki/Search_and_rescue)
  * [Cargo and Relief Delivery](https://en.wikipedia.org/wiki/Delivery_drone)
* Environmental Protection **XXX**
  * Wildlife Preservation (e.g. Anti-Poaching)
  * Wilderness Protection (e.g. Forest Fire Detection)
* Patrol **XXX**
  * Border Patrol
  * Smuggling Control

### Proprietary soft/hard-ware components of the AUAV
List of the components that enable the autonomy of our drones and the functionalities required by the assignments, which in turn engender the ethical issues to be addressed in the later sections.

* Advanced thermalgraphic and HD cameras
* Satellite Internet access
* Autonomous AI systems designed for each specific objective
* Advanced speech/graphical interfaces
* "Smart" data storage device that logs the drone's sensor and activity data
* "Swarm intelligence" that allows multiple AUAVs to collarborate efficiently in a mission

# 2. Main ethical concerns

##The norms to which the design process of **XXX** conforms
In alignment with the goal of serving humanitarian purposes, there are some acknowledged norms which the design process of **XXX** must conform to, including (but not limited to) the following:

### Four of the seven fundamental principles of the International Red Cross and Red Crescent Movement
* __Humanity__
* __Impartiality__
* __Neutrality__
* __Independence__

#### Humanity
> (...) bring assistance without discrimination to the wounded on the battlefield, endeavours, in its international and national capacity, to prevent and alleviate human suffering wherever it may be found. Its purpose is to protect human life and health and to ensure respect for the human being. It promotes mutual understanding, friendship, cooperation and lasting peace amongst all people.

#### Impartiality
> It makes no discrimination as to nationality, race, religious beliefs, class or political opinions. It endeavours to relieve the suffering of individuals, being guided solely by their needs, and to give priority to the most urgent cases of distress.

#### Neutrality
> In order to continue to enjoy the confidence of all, the movement may not take sides in hostilities or engage at any time in controversies of a political, racial, religious or ideological nature.

#### Independence
> The Movement is independent. The National Societies, while auxiliaries in the humanitarian services of their governments and subject to the laws of their respective countries, must always maintain their autonomy so that they may be able at all times to act in accordance with the principles of the Movement.

### General principles outlined by IEEE's Ethically Aligned Design
* __Human Benefit__
* __Responsibility__
* __Transparency__
* __Education and Awareness__

## Ethical issues to be addressed in the design process
#### Lack of transparency
###### poor documentation
Besides documentations of the software architecture, the data flows, the testing results and the performance and limitations, it is equally important for the designers of software systems to document the ethical concerns of the design, as well as empirical evidence of efforts and methodology used to resolve these issues.
###### exaggeration on AI capability
A faulty but common practice has been to exaggerate on the capability of autonomous artificial intelligence systems, thus creating a gap between how they are marketed and their actual performance. Hence, it is the engineer's as well as marketer's responsibility to close the gap as much as possible. Also, we need to constantly validate and improve our certification scheme for our AI systems to ensure the technologies have been independently assessed as being safe and ethically sound.
 
###### the blackbox
Currently a big part of our AI systems is developed using the Deep Learning technology, which is notorious for its "blackbox" characteristic. This particular machine learning method produces state-of-the-art results, but the functioning of which even the developers often do not fully understand. Hence, it is the responsibility of our engineers to:

1. Design fail-safe measures to take over the drone's decision-making logic in the event of unintended behavior or extremely adversarial circumstance. (For instance, during extreme weather, maneuvering in the woods might be overly risky, and the drone should "know" to temporarily stay away from such terrains.)
2. Persistently research and publish their study on the underlying mathematical and statistical principles that rationalize the AI system's design and decision making process, and accept liability for the ethical complications resulted from the system's unexpected behavior.

#### Lack of impartiality
When designing the AI system, the developers might unintentionally inject biases into the system. For instance, the sensor system used to detect a human probably should not make the assumption that all humans have two arms and/or two legs; the speech/graphical interface used to communicate with a person of interest should not have an intellectual or language threshold that disfavors a certain population; another example would be a facial recognition system trained entirely on Caucasian faces may work incorrectly or not at all on people with non-Caucasian skin tones or facial structures.

We recommend designers familiarize themselves with relevant resources specific to the target population.

#### Unintended or unexpected behaviors, including hacking
AI research teams should put a significant amount of efforts into AI safety research as capabilities grow. These efforts should manifest themselves as pre-emptive safefy measures against any form of appropriation, hacking, and sabotaging intention at the soft/hard-ware system of the AUAV. They should cultivate a “safety mindset”, and better understand many of these problems by studying adversarial examples.

We also recommend that all AI research teams seek to pursue the following goals, all of which seem likely to help avert the aforementioned problems:

1. Contribute to research on concrete problems in AI safety, such as those described by Amodei et al. in [Concrete Problems in AI Safety](https://arxiv.org/abs/1606.06565) and Taylor et al. in [Alignment for Advanced Machine Learning Systems](https://intelligence.org/2016/07/27/alignment-machine-learning/)
2. Work to build safe and secure environments in which potentially unsafe AI systems can be developed and tested. In particular, we recommend that AI research teams develop, share, and contribute to AI safety test environments and tools and techniques for “boxing” AI systems (see Babcock et al. [2016](https://link.springer.com/chapter/10.1007%2F978-3-319-41649-6_6) and Yampolskiy [2012](http://www.ingentaconnect.com/content/imp/jcs/2012/00000019/F0020001/art00014) for preliminary work).
3. Ensure that AI systems are corrigible in the sense that the systems are amenable to shutdown and modification by the remote operators.

#### Lack of protection for personal data 
Much of the contention associated with the concept of “privacy” actually relates to access and consent. The challenges are often around transparency and providing an explicit understanding of the consequences of agreeing to the use of our personal data, complicated by the data handling processes behind true “consent.” Privacy rights are often not respected in the design and business model of services using said data.

To resolve the issue of offering adequate protection for personal data, designers and developers should consider using “Privacy-by-Design”/Privacy-by-Default methodologies (referring to the practice or business philosophy of privacy embedded in the development of a service). Paradigms like “[differential privacy](https://www.wired.com/2016/06/apples-differential-privacy-collecting-data/)” may also allow for designers and developers to bake privacy into the design and development of services. Differential privacy shifts the focus from “your data” to finding general usage patterns across larger data sets. It uses hashing, sub-sampling, and noise- injection techniques to obfuscate personal information about individuals.

As a tool for any organization regarding these issues, a good starting point is to apply the who, what, why, and when test to the collection and storage of personal information:

1. Who requires access and for what duration— is it a person, system, regulatory body, or legal requirement?
2. What is the purpose for the access—is it read, use and discard or collect, use and store?
3. Why is the data required—is it to fulfill compliance, lower risk, because it is monetized, or in order to provide a better service/experience?
4. When will it be collected, for how long will it be kept, when will it be discarded, updated, re-authenticated—how does duration impact the quality and life of the data?
