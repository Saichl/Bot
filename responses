import base64
import requests
from openai import OpenAI

from config import TOKEN_OPENAI


client = OpenAI(api_key=TOKEN_OPENAI)


def get_response(user_input: str):
    response = client.chat.completions.create(
        model="gpt-4o-mini",
        messages=[
            {"role": "system", "content": f"{user_input}"},
        ]
    )
    answer = response.choices[0].message.content
    print(answer)
    return answer
