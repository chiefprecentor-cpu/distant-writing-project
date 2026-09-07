# Governance Background: Third-Party SDKs, Data Infrastructure and Inferential Sensitivity

## Status

This is a data-governance background candidate that is not currently being developed. It preserves the narrative value of third-party infrastructure, sensor permissions and inferentially sensitive data; it does not confirm that any real application has actually collected, shared or misused any category of data.

## From Visible Applications to Invisible Infrastructure

The user faces an app or service, but the actual data and action chain may include:

- the host application and its first-party code;
- login, payment, advertising, analytics, attribution, push-notification, crash-reporting or social-sharing SDKs;
- operating-system permissions, sensor interfaces that do not require explicit authorisation, and background components;
- SDK providers, parent companies, data processors, cloud services and data-broker networks;
- features, profiles, audience labels and model outputs formed from raw behaviour;
- advertisers, platforms, employers, insurers or public institutions that finally act on the basis of outputs.

This chain is suitable for showing how responsibility is dispersed: each party claims that it only provides a small function, while the whole forms a data infrastructure that users can hardly see, understand or refuse.

## Evidence Strength Must Be Layered

- A permission declared in a manifest can only prove that the application requests or may use it; it does not prove that it is necessarily called at runtime.
- Detecting an SDK or component can only prove that code or configuration exists; it does not prove that a certain kind of data has already been transmitted, who received it, or what purpose it was used for.
- Two applications containing the same SDK does not prove that they shared a specific user's content, identity or profile.
- Seeing related content after a conversation is not enough to prove that a device was eavesdropping; shared location, search behaviour, contacts, the advertising ecosystem, selective memory or other routes may all produce similar experiences.
- Inferring real data flows from static code requires combination with evidence such as dynamic network observation, versions, permission state, privacy notices and backend behaviour.

These boundaries are useful not only for real-world research, but also for making investigative plots in the novel more credible: characters may first discover risk clues from permissions or components, but they cannot immediately treat clues as completed accusations.

## From Ordinary Behaviour to Inferentially Sensitive Features

Viewing, dwelling, swiping, device movement, location proximity and content interaction appear ordinary, but once combined they may be used by models to infer political tendency, health status, sexual orientation, economic vulnerability or other sensitive features. What truly produces differentiated treatment may not be raw records, but invisible embeddings, scores, similar populations or commercial labels.

Three distinctions still need to be maintained:

- a model being able to infer something does not mean the inference is correct;
- an inference being ethically sensitive does not mean it already has the same legal classification in every jurisdiction;
- an SDK can become infrastructure in a data chain, but this does not mean that every SDK independently completes all profiling or sells labels.

## Sensors and Interaction Control

Some sensor access may not appear as a "dangerous permission" popup familiar to users, yet it can be used for advertising redirects, fingerprinting, activity inference or other interactions. Its risk lies not only in secret collection, but also in using bodily movement to trigger pages, purchase flows or attention shifts that users do not want.

If this enters a literary plot, the break between "the device merely sensed a shake" and "the commercial system interpreted that shake as consent or interest" can be written out; the concrete technical implementation or permission level cannot be fixed while it remains unresearched.

## Relation to Existing Themes

- It adds the infrastructure layer of how data flows from dispersed applications into a governance assemblage for [Algorithmic Governance: Population Mapping, Social Sorting and `in situ`](算法治理_群体映射社会分拣与in_situ.md).
- It explains that highly mature behavioural collection and commercial profiling may still lack causal knowledge of how characters form action in new situations, and therefore does not refute the data insufficiency in [Global Base: Real Enumeration and Meta-Time](../creative_work/story_state/全局底座_真实枚举与元时间.md).
- It can also become the everyday background of an early Anthropocene worldline, without needing to downgrade the terminal AI into an advertising tracking system.

## Use Boundary

This candidate does not point to any specific real app, company, SDK or person, and does not prove that any real data flow exists. If concrete permissions, components, data flows or legal classifications enter the work or dissertation, they must be rechecked against reliable public materials.
