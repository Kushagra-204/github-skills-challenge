# GitHub Challenge

<img src="https://octodex.github.com/images/Professortocat_v2.png" align="right" height="200px" />

Hey there!

Your challenge is ready.
Follow the instructions provided for this challenge and complete the required tasks in this repository.

Make sure your work is committed and pushed to your repository before submission.

Good luck!


---

&copy; 2025 GitHub &bull; [Code of Conduct](https://www.contributor-covenant.org/version/2/1/code_of_conduct/code_of_conduct.md) &bull; [MIT License](https://gh.io/mit)



These are real issues in the project:

1. in aiops_pipeline.py

    Issue:
    Producer publishes to one topic
    Consumer reads from another topic

    wrong code
    producer_topic = EventTopic("service-events")
    ...
    consumer_topic = EventTopic("anomaly-events")

    correct code
    topic = EventTopic("anomaly-events")
    producer = EventProducer(topic)
    consumer = EventConsumer(topic)

2. in anomaly_detector.py
    Issue:
    The code checks for "WARNING" instead of "ERROR"

    wrong code
    if record["log_level"] == "WARNING":
    reasons.append("Error log detected")

    correct code
     # INTENTIONAL ASSESSMENT ISSUE
    if record["log_level"] == "ERROR":
    reasons.append("Error log detected")