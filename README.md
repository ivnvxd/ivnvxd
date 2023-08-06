```python
class Dev:
    def __init__(self):
        self.name = "Andrey"
        self.languages = ["ru-RU", "en-US", "de-DE"]
        self.role = "Software Engineer"
        self.skills = ["Python", "Go", "Django", "Flask", "SQL", "JS", "HTML", "CSS"]

    def generate_readme(self):
        intro = (
            f"# Hello world! :wave: My name is {self.name}\n"
            + f"I'm a {self.role} with Product Management and Entrepreneurship background."
        )
        skills = "## :rocket: My Tech Stack:\n```\n" + f"{', '.join(self.skills)}\n```"

        return f"{intro}\n{skills}"


me = Dev()
print(me.generate_readme())
print("Let's connect and build amazing things together! :wink:")
```
