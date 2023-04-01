```python
class Person:

    def __init__(self):
        self.name = 'Andrey'
        self.languages = ['ru-RU', 'en-US', 'de-DE']


class SoftwareEngineer(Person):

    def __init__(self):
        super().__init__()
        self.role = 'Python developer'
        self.skills = {
            'code': ['Python', 'Go', 'SQL', 'HTML', 'CSS'],
            'tools': ['Django', 'Flask', 'PostgreSQL', 'Redis', 'NumPy', 'Pandas', 'Docker', 'Git']
        }

    def introduce(self):
        intro = f"Hello world! :wave: My name is **{self.name}**, "
        intro += f"and I'm a **{self.role}** with a background in product management and entrepreneurship.\n"
        intro += "And I love to connect with different people. Feel free to reach out to me!\n"
        return intro

    def display_skills(self):
        skills = "## :rocket: Technical Skills\n\n```python\n{\n"
        skills += f'    "code": {self.skills["code"]},\n'
        skills += f'    "tools": {self.skills["tools"]}\n'
        skills += "}\n```\n"
        return skills

    def get_in_touch(self):
        return (
            "## :mailbox_with_mail: Get In Touch\n\n"
            "- [LinkedIn](https://www.linkedin.com/in/abivanov/)\n"
            "- [Facebook](https://www.facebook.com/andrey.ivanov.194)\n"
            "- [Email](mailto:ivnv.xd@gmail.com)\n"
        )

    def generate_readme(self):
        readme = self.introduce() + "\n"
        readme += self.display_skills() + "\n"
        readme += self.get_in_touch() + "\n"
        readme += "---\n\n"
        readme += "Let's connect and build amazing things together! :wink:"
        return readme


me = SoftwareEngineer()
readme = me.generate_readme()
print(readme)
```
