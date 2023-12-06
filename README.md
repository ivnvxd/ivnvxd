```elixir
defmodule Dev do
  @moduledoc """
  Generates a README profile for a developer.
  """

  defstruct name: "Andrey",
            languages: ["ru-RU", "en-US", "de-DE"],
            role: "Software Engineer",
            experience: ["Product Management", "Finance", "Entrepreneurship"],
            skills: ["Python", "Go", "Elixir", "Django", "Flask", "SQL"]

  @doc """
  Generates a README string for a developer's GitHub profile.
  """
  def generate_readme(%Dev{name: name, role: role, experience: experience, skills: skills}) do
    [last | rest] = Enum.reverse(experience)
    experiences = Enum.join(Enum.reverse(rest), ", ") <> ", and " <> last

    intro =
      "# Hello world! :wave: My name is #{name}\n" <>
        "I'm a #{role} with #{experiences} background."

    skills_text = "## :rocket: My Tech Stack:\n```\n" <> Enum.join(skills, ", ") <> "\n```"
    connect_text = "Let's connect and build amazing things together! :wink:"

    intro <> "\n" <> skills_text <> "\n" <> connect_text
  end
end

me = %Dev{}
IO.puts(Dev.generate_readme(me))
```