```elixir
defmodule Dev do
  defstruct name: "Andrey",
            languages: ["ru-RU", "en-US", "de-DE"],
            role: "Software Engineer",
            experience: ["Product Management", "Finance", "Entrepreneurship"],
            skills: ["Python", "Go", "Elixir", "Django", "Flask"]

  def generate_readme(%Dev{name: name, role: role, experience: experience, skills: skills}) do
    experiences_text =
      experience |> Enum.reverse() |> format_experience_list()

    skills_text = Enum.join(skills, ", ")

    "# Hello world! :wave: My name is #{name}\n" <>
      "I'm a #{role} with #{experiences_text} background.\n\n" <>
      "## :rocket: My Tech Stack:\n```\n#{skills_text}\n```\n" <>
      "Let's connect and build amazing things together! :wink:"
  end

  defp format_experience_list([last | rest]) do
    Enum.join(Enum.reverse(rest), ", ") <> ", and " <> last
  end

  def run do
    me = %Dev{}
    IO.puts(generate_readme(me))
  end
end
```