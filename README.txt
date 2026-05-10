{
  "nbformat": 4,
  "nbformat_minor": 0,
  "metadata": {
    "colab": {
      "provenance": [],
      "authorship_tag": "ABX9TyNpc35sU8uyKNyP1FG/Xu5C",
      "include_colab_link": true
    },
    "kernelspec": {
      "name": "python3",
      "display_name": "Python 3"
    },
    "language_info": {
      "name": "python"
    }
  },
  "cells": [
    {
      "cell_type": "markdown",
      "metadata": {
        "id": "view-in-github",
        "colab_type": "text"
      },
      "source": [
        "<a href=\"https://colab.research.google.com/github/eloelo5057/kurs_AI/blob/main/README.txt\" target=\"_parent\"><img src=\"https://colab.research.google.com/assets/colab-badge.svg\" alt=\"Open In Colab\"/></a>"
      ]
    },
    {
      "cell_type": "markdown",
      "source": [
        "# **podstawowe elementy języka python**\n",
        "*W tym rozdziale przedstawimy podstawowe elementy skaładni języka python*\n",
        "---\n",
        "\n",
        "### [dokumentacja python](https://www.python.org)\n",
        "---\n",
        "Omawiane elementy:\n",
        "\n",
        "1. Zmienne\n",
        "---\n",
        "2. Listy\n",
        "---\n",
        "3. Pętle\n",
        "---\n",
        "4. Słowniki i krotki\n",
        "---\n",
        "5. Instrukcje warunkowe\n",
        "---\n",
        "6. Funkcje\n",
        "---\n",
        "7. Obsługa plików\n",
        "---\n",
        "8. Obsługa wyjątków\n",
        "---\n",
        "6. Przesuwamy nową sekcję maksymalnie na górę\n",
        "---\n",
        "7. Analiza ustawień (zmiana motywu, czcionki, szerokość wcięć)\n",
        "---\n",
        "8. Środowisko\n",
        "---\n"
      ],
      "metadata": {
        "id": "VFNFatJb-6lS"
      }
    },
    {
      "cell_type": "code",
      "source": [
        "!git init\n",
        "!git config --global user.name \"eloelo5057\"\n",
        "!git config --global user.email \"piotrus.kolecki@outlook.com\""
      ],
      "metadata": {
        "colab": {
          "base_uri": "https://localhost:8080/"
        },
        "collapsed": true,
        "id": "ws2XtcD5E92I",
        "outputId": "2c455024-645d-4f8e-c29b-3777d9a5655d"
      },
      "execution_count": null,
      "outputs": [
        {
          "output_type": "stream",
          "name": "stdout",
          "text": [
            "Reinitialized existing Git repository in /content/.git/\n"
          ]
        }
      ]
    },
    {
      "cell_type": "code",
      "source": [
        "!git add ."
      ],
      "metadata": {
        "id": "W14-LJn_Fsoo"
      },
      "execution_count": null,
      "outputs": []
    },
    {
      "cell_type": "code",
      "source": [
        "!git commit -m \"Inincjalizacja projektu\""
      ],
      "metadata": {
        "colab": {
          "base_uri": "https://localhost:8080/"
        },
        "collapsed": true,
        "id": "JX-QmyCiF5JR",
        "outputId": "d73b61b8-f80a-4396-fc11-a1aed74b8424"
      },
      "execution_count": null,
      "outputs": [
        {
          "output_type": "stream",
          "name": "stdout",
          "text": [
            "On branch main\n",
            "nothing to commit, working tree clean\n"
          ]
        }
      ]
    },
    {
      "cell_type": "code",
      "source": [
        "!git branch -M main\n"
      ],
      "metadata": {
        "id": "Q5K3DzX_GDO_"
      },
      "execution_count": null,
      "outputs": []
    },
    {
      "cell_type": "code",
      "source": [
        "!git remote add origin https://pat@github.com/eloelo5057/kurs_AI.git"
      ],
      "metadata": {
        "colab": {
          "base_uri": "https://localhost:8080/"
        },
        "collapsed": true,
        "id": "Ai1NBKEUJQW2",
        "outputId": "78057e50-faab-44ee-ff62-c5c06aa8f69c"
      },
      "execution_count": null,
      "outputs": [
        {
          "output_type": "stream",
          "name": "stdout",
          "text": [
            "error: remote origin already exists.\n"
          ]
        }
      ]
    },
    {
      "cell_type": "code",
      "source": [
        "!git push -u origin main"
      ],
      "metadata": {
        "colab": {
          "base_uri": "https://localhost:8080/"
        },
        "collapsed": true,
        "id": "9kPzIQkVJ83o",
        "outputId": "b7893777-1abc-42c6-b9af-074868144e28"
      },
      "execution_count": null,
      "outputs": [
        {
          "output_type": "stream",
          "name": "stdout",
          "text": [
            "Enumerating objects: 28, done.\n",
            "Counting objects:   3% (1/28)\rCounting objects:   7% (2/28)\rCounting objects:  10% (3/28)\rCounting objects:  14% (4/28)\rCounting objects:  17% (5/28)\rCounting objects:  21% (6/28)\rCounting objects:  25% (7/28)\rCounting objects:  28% (8/28)\rCounting objects:  32% (9/28)\rCounting objects:  35% (10/28)\rCounting objects:  39% (11/28)\rCounting objects:  42% (12/28)\rCounting objects:  46% (13/28)\rCounting objects:  50% (14/28)\rCounting objects:  53% (15/28)\rCounting objects:  57% (16/28)\rCounting objects:  60% (17/28)\rCounting objects:  64% (18/28)\rCounting objects:  67% (19/28)\rCounting objects:  71% (20/28)\rCounting objects:  75% (21/28)\rCounting objects:  78% (22/28)\rCounting objects:  82% (23/28)\rCounting objects:  85% (24/28)\rCounting objects:  89% (25/28)\rCounting objects:  92% (26/28)\rCounting objects:  96% (27/28)\rCounting objects: 100% (28/28)\rCounting objects: 100% (28/28), done.\n",
            "Delta compression using up to 2 threads\n",
            "Compressing objects: 100% (21/21), done.\n",
            "Writing objects: 100% (28/28), 8.42 MiB | 2.00 MiB/s, done.\n",
            "Total 28 (delta 4), reused 0 (delta 0), pack-reused 0\n",
            "remote: Resolving deltas: 100% (4/4), done.\u001b[K\n",
            "To https://github.com/eloelo5057/kurs_AI.git\n",
            " * [new branch]      main -> main\n",
            "Branch 'main' set up to track remote branch 'main' from 'origin'.\n"
          ]
        }
      ]
    },
    {
      "cell_type": "markdown",
      "source": [
        "# Zmienne\n",
        "---\n"
      ],
      "metadata": {
        "id": "6JrJczFcMQy8"
      }
    },
    {
      "cell_type": "code",
      "source": [
        "liczba = 6\n",
        "zmiennoprzecinkowa = 8.9\n",
        "napis = \"Tekst:)\"\n",
        "logiczne = True\n",
        "\n",
        "print(f\"int: {liczba}, Float: {zmiennoprzecinkowa}, string: {napis}, boolean: {logiczne}\")"
      ],
      "metadata": {
        "id": "SoChgBiZMq8U"
      },
      "execution_count": null,
      "outputs": []
    },
    {
      "cell_type": "markdown",
      "source": [
        "# Listy\n",
        "---\n",
        "- zawierają elementy\n",
        "- Elementy różnego rozmiaru\n",
        "- Indeksowanie (mają określoną kolejnośc)"
      ],
      "metadata": {
        "id": "Uo-Z5DzRNUOO"
      }
    },
    {
      "cell_type": "code",
      "source": [
        "gry = [\"xplane\", \"Minecraft\", \"LOL\"]\n",
        "\n",
        "print(gry)\n",
        "print(f\"Pierwszy element: {gry[0]}\")\n",
        "\n",
        "print(f\"Długość listy: {len(gry)}\")\n",
        "\n",
        "gry.append(\"Roblox\")\n",
        "print(gry)"
      ],
      "metadata": {
        "id": "1UHVtuyKNzsr"
      },
      "execution_count": null,
      "outputs": []
    },
    {
      "cell_type": "code",
      "source": [
        "from google.colab import drive\n",
        "drive.mount('/content/drive')"
      ],
      "metadata": {
        "id": "ZNVvLN8fP91e"
      },
      "execution_count": null,
      "outputs": []
    },
    {
      "cell_type": "code",
      "source": [],
      "metadata": {
        "id": "PX8BiUcUNYuL"
      },
      "execution_count": null,
      "outputs": []
    }
  ]
}