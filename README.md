```elixir
defmodule Dev do
  @moduledoc """
  Represents a developer's profile and generates a formatted README.
  """

  defstruct name: "Andrey",
            languages: ["ru-RU", "en-US", "de-DE"],
            role: "Software Engineer",
            experience: ["Product Management", "Finance", "Entrepreneurship"],
            skills: ["Python", "Go", "Elixir", "Django", "Flask"]

  @doc """
  Generates a README string for GitHub profile.
  """
  def generate_readme(%Dev{name: name, role: role, experience: experience, skills: skills}) do
    experiences_text = format_experience_list(experience)
    skills_text = Enum.join(skills, ", ")

    "# Hello world! :wave: My name is #{name}\n" <>
      "I'm a #{role} with #{experiences_text} background.\n" <>
      "## :rocket: My Tech Stack:\n```\n#{skills_text}\n```\n" <>
      "Let's connect and build amazing things together! :wink:"
  end

  @doc """
  Formats a list of experiences into a string.
  """
  defp format_experience_list(experience) do
    [last | rest] = Enum.reverse(experience)
    Enum.join(Enum.reverse(rest), ", ") <> ", and " <> last
  end
end

me = %Dev{}
IO.puts(Dev.generate_readme(me))
```