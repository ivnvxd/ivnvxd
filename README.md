```python
class Person:
    def __init__(self):
        self.name = "Andrey"
        self.languages = ["ru-RU", "en-US", "de-DE"]


class SoftwareEngineer(Person):
    def __init__(self):
        super().__init__()
        self.role = "Software Developer"
        self.skills = {
            "code": ["Python", "Go", "HTML", "CSS"],
            "tools": ["Django", "Flask", "SQL", "NoSQL", "NumPy", "Docker"],
        }

    def generate_readme(self):
        intro = (
            f"Hello world! :wave: My name is **{self.name}**, "
            + f"and I'm a **{self.role}** "
            + "with Product Management and Entrepreneurship background."
        )

        skills = (
            "## :rocket: Tech Skills:\n\n```python\n"
            + '{\n    "code": ' + ", ".join(self.skills["code"])
            + ',\n    "tools": ' + ", ".join(self.skills["tools"])
            + "\n}\n```"
        )

        return (
            f"{intro}\n\n{skills}\n\n"
            + "Let's connect and build amazing things together! :wink:"
        )


me = SoftwareEngineer()
print(me.generate_readme())
```
