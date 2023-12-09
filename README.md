```elixir
defmodule Dev do
  @type t :: %Dev{
          name: String.t(),
          role: String.t(),
          speak: %{optional(String.t()) => String.t()},
          exp: list(String.t()),
          skills: list(String.t())
        }
  defstruct name: "Andrey",
            role: "Software Engineer",
            speak: %{"ru-RU" => "Russian", "en-US" => "English", "de-DE" => "German"},
            exp: ["Product Management", "Finance", "Entrepreneurship"],
            skills: ["Python", "Go", "Elixir", "Django", "Flask"]
end

defmodule GenerateReadme do
  @spec generate_readme(Dev.t()) :: String.t()
  def generate_readme(%Dev{name: name, role: role, exp: exp, speak: speak, skills: skills}) do
    [
      "# Hello world! :wave: My name is #{name}.",
      "I'm a #{role} with #{format_list(exp)} background.",
      "I speak #{format_list(Map.values(speak))}.\n",
      "## :rocket: My Tech Stack:\n```\n#{Enum.join(skills, ", ")}\n```",
      "Let's connect and build amazing things together! :wink:"
    ]
    |> Enum.join("\n")
  end

  @spec format_list(list(String.t())) :: String.t()
  defp format_list([single]), do: single
  defp format_list(list) do
    Enum.split(list, -1)
    |> (fn {rest, [last]} -> Enum.join(rest, ", ") <> ", and " <> last end).()
  end

  @spec run() :: :ok
  def run do
    me = %Dev{}
    IO.puts(generate_readme(me))
  end
end
```