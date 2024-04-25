These markdown documents can later be used as input for an AI in combination with the right plugins, instead of writing the exact procedural code. Advantage being it's much more readable.

This is an in-between step from ambient AI voice input to an agent, where first, we try to describe wishes of the human in a single succinct description, before it gets turned into an OpenAPI/Agent.

This would be the process to turn a markdown file into an agent (itself also being an example of a Natural Language Procedure):

1. Determine what actions are needed to be performed
2. Look up those actions, incase you don't find all, determine to either go smaller or reorganise the actions into a different shape.
3. Once we have all actions as openapi operations, determine the structure of one or multiple agents to perform these actions, to make the final agent super unambiguous and
4. Give the agent creator agent access to all tools such as combination-proxy creation, agent-openapi-creation, and let it do its thing
5. The final result should be an Agent OpenAPI specification that can perform the task of the procedure, as good as possible.
