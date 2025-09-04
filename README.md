# streamlit_tutorial

> 📨 **New! Prefer guided support?**  
> 👉 Sign up for the [free email course](https://arilamstein.com/blog/2025/09/02/free-course-learn-to-build-data-apps-with-streamlit/) to learn Streamlit step-by-step—with help when you need it.

----

This repository walks you through creating and deploying a data app in Python using
[Streamlit](https://streamlit.io/). It contains:
  * A motivating example. What problem does Streamlit solve?
  * A small demo app to get you started. This app contains interesting, real-world data.
  * Instructions for installing, running, and modifying the demo app on your local machine.
  * Exercises for improving the app. Solving these problems will help you learn Streamlit.
  * Instructions for deploying your finished app to the internet. This will let you share it with friends and family.

You can view the final app you will build [here](https://arilamstein-tutorial.streamlit.app/).

### Prerequisites

This tutorial assumes that you have prior experience with git, the command line, and Python. 

### How to Take This Course

If you've taught yourself new Python packages before, you might be able to complete this tutorial by yourself in an afternoon.

After teaching this material at a local meetup, I noticed many participants benefited from checking in with me after each section. To support learners at scale, I created a free email version of the course. Over 7 days, you’ll receive one email per day with focused instructions—and if you get stuck, just hit “reply” and I’ll help you troubleshoot.

To sign up, visit: [Free Course: Learn to Build Data Apps with Streamlit!](https://arilamstein.com/blog/2025/09/02/free-course-learn-to-build-data-apps-with-streamlit/)

### Motivating Example

I frequently use Jupyter Notebooks to convey analytical results. Each notebook typically imports a dataset,
transforms it, and then presents a visualization or two. In short, each notebook tells a story about a dataset.

Streamlit lets me convert the code in my notebooks to a web application. Instead of telling a story, I am now giving people a
tool to explore the dataset themselves. 

Click [here](motivating_example.ipynb) to see an example.

### Setup

This tutorial uses [uv](https://docs.astral.sh/uv/) to manage the project's virtual environment. To install uv:
1. Open a terminal.
1. Follow the installation instructions [here](https://docs.astral.sh/uv/#installation). 
1. Restart your terminal.

Next fork and clone this repository:
1. Fork this repository in Github
   ([instructions](https://docs.github.com/en/pull-requests/collaborating-with-pull-requests/working-with-forks/fork-a-repo?tool=desktop)). Having your own fork is necessary to deploy your app, which is the last step in this tutorial.
1. Clone your fork to your local machine ([instructions](https://docs.github.com/en/repositories/creating-and-managing-repositories/cloning-a-repository)).

Finally, create the virtual environment for the project:
1. In your project directory, type `uv sync`. This will create a virtual environment in the project's `.venv` directory. That virtual environment will have same version of Python I used when creating this project, as well as all the packages you need to complete the workshop. 

The above instructions need to be executed just once.

### Run the Demo App

To confirm that the Setup was successful, see if you can run the demo app:

1. First activate the project's virtual environment: In the terminal, navigate to the project's directory and type `source .venv/bin/activate`.
1. Then type `streamlit run streamlit_app.py`.

A browser should open that contains the demo app. It should look like this:
<p align="center">
  <img src="screenshot-demo-app.png" alt="Demo App Screenshot" width="50%">
</p>

### Streamlit Basics

You're now ready to start coding! Let's start with the basics.

1. While the app is running, open the file [streamlit_app.py](streamlit_app.py). Can you guess what each line of
   the file does?
1. Streamlit apps can reload after you make changes to the source code. That is, you don't need to stop and restart the app to
   see the result of your changes. 
    1. While the app is running, change the text in the
   `st.header` call (line 7) to be "Changes in US State Demographics Over Time". Save the file. 
    1. The app should now have
   a button in the upper right that says "Rerun". Click it. The app should update with the new text.
   
### Modify the App 

The best way to learn Streamlit is to solve small, real-world problems on an existing app. Open the file
[exercises.md](exercises.md) and try to complete the tasks listed there. They ask you to modify the demo app by:
1. Adding a new graph.
1. Adding a new input widget.
1. Using the value from input widgets when creating a graph. 
1. Using tabs to make the app easier to navigate. 

These are common tasks when working in Streamlit. If you get stuck, check my solutions in `solution_app.py`.

After you have finished the exercises, commit your changes and push them to Github.

### Deploy Your App

Streamlit makes it easy to share your app with others. Once you've pushed your code to GitHub, follow these steps to deploy it to the web:

1. Go to [streamlit.io/cloud](https://streamlit.io/cloud) and sign in with GitHub.
2. Click **"New app"** and select:
   - Your repository
   - The correct branch (i.e. `main`)
   - The entry point file (i.e. `streamlit_app.py`)
3. Click **"Deploy"** and your app will go live!

### 🔁 Updating Your App

After the initial deployment, **any changes you push to GitHub will automatically redeploy your app**.

I encourage you to share your app with friends and family!

### A More Complex App

This tutorial is based on the first app I built with Streamlit. I call that app the "Covid Demographics Explorer", and
it helps people understand how US counties changed since Covid-19. You can view it
[here](https://census-explorer.streamlit.app/). 

While that app is more complex than the app you just built, most of the complexity is in the data and visualizations.
That is, it uses
Streamlit in much the same way as the app you just created:
  * It loads data on startup.
  * It has input widgets.
  * Those widgets determine what graphs are shown.
  * The graphs are separated by tabs.

You now know enough Streamlit to build and deploy fairly interesting apps. I look forward to seeing what you create!

### Conclusion

Congratulations: You have now cloned, modified, and deployed your first Streamlit app!

If you found this tutorial helpful, please give the repo a star and share it with your friends. 

If you have feedback on the tutorial, feel free to reach out via my website: [AriLamstein.com](https://arilamstein.com/).