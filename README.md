<div align="center">

<!-- Header -->
<img src="https://capsule-render.vercel.app/api?type=waving&color=0:2D8BB0,100:ADB1B5&height=220&section=header&text=RS%20ABHISHEK&fontSize=52&fontColor=061A33&fontAlignY=45&%7C%20ISE%20%7C%20ENGINEERING&descSize=25&descAlignY=68&descColor=061A33" width="100%"/>

<h1 align="center">
  <a href="https://git.io/typing-svg">
    <img
      src="https://readme-typing-svg.demolab.com?font=JetBrains+Mono&weight=500&size=40&duration=3000&pause=1000&color=00AEEF&center=true&vCenter=true&width=700&lines=IS+Engineering+Student"
      alt="IS Engineering Student"
    />
  </a>
</h1>

<br>

<br>

<!-- Social Buttons -->

<a href="https://github.com/RS ABHISHEK">
  <img src="https://img.shields.io/badge/GITHUB-0D1117?style=for-the-badge&logo=github&logoColor=00AFFF" />
</a>
<a href="https://www.linkedin.com/in/rs-abhishek-179753432/">
  <img src="https://img.shields.io/badge/LINKEDIN-0A8ED9?style=for-the-badge&logo=linkedin&logoColor=white" />
</a>
<a href="mailto:YOUR_EMAIL@gmail.com">
  <img src="https://img.shields.io/badge/GMAIL-EF4035?style=for-the-badge&logo=gmail&logoColor=white" />
</a>
<img src="https://komarev.com/ghpvc/?username=rsabhishek&label=Profile%20Views&color=38A9D5&style=for-the-badge" />

<br><br>

<hr style="border: 1px solid white; width: 80%;">

</div>


# 👋 Hi, I'm RS ABHISHEK

### 💻 Developer | Programmer | Video Editor

I'm **RS ABHISHEK**, passionate about programming, web development, and building creative projects.

---

## 👨‍💻 About Me

🎓 Currently pursuing Information Science & Engineering

💻 Building software and exploring different technologies

🌱 Continuously learning and improving my development skills

🎬 Interested in video editing

💡 Enjoy solving problems and creating useful projects

🔍 Always curious to explore new tools and technologies

## 🛠️ Skills & Technologies

<p align="left">
<img src="https://skillicons.dev/icons?i=c,cpp,python,java,html,css,js,react,git,github,vscode,linux" />
</p>


---

## 🔥 GitHub Streak

<p align="center">
<img src="https://streak-stats.demolab.com/?user=YOUR_USERNAME&theme=tokyonight" />
</p>



---

<h3 align="center">✨ Thanks for visiting my profile! ✨</h3>

<h4 align="center">Keep Coding • Keep Learning • Keep Building 🚀</h4>



---

```python
from manimlib import *


class ProfileAnimation(Scene):
    def construct(self):

        # ---------------------------------------------------------
        # CUSTOMIZE YOUR PROFILE HERE
        # ---------------------------------------------------------
        NAME = "YOUR NAME"
        ROLE = "Developer • Designer • Creator"

        ABOUT = [
            "💻 Software Developer",
            "🚀 Building cool projects",
            "🧠 Learning something new every day",
        ]

        SKILLS = [
            "Python",
            "JavaScript",
            "React",
            "Git",
            "Machine Learning",
        ]

        GITHUB = "github.com/YOUR_USERNAME"
        # ---------------------------------------------------------


        # Background
        self.camera.background_color = "#0D1117"


        # =========================================================
        # 1. INTRO
        # =========================================================

        hello = Text(
            "Hello, World!",
            font_size=64,
            color=BLUE_B,
        )

        self.play(
            Write(hello),
            run_time=1.5
        )

        self.wait(0.5)

        self.play(
            hello.animate.scale(0.55).to_edge(UP),
            run_time=1
        )


        # =========================================================
        # 2. NAME
        # =========================================================

        name = Text(
            NAME,
            font_size=72,
            color=WHITE,
        )

        underline = Line(
            LEFT * 3,
            RIGHT * 3,
            color=BLUE_B,
        )

        underline.next_to(name, DOWN, buff=0.2)

        self.play(
            FadeIn(name, shift=UP * 0.4),
            Create(underline),
            run_time=1.2
        )

        role = Text(
            ROLE,
            font_size=30,
            color=GREY_B,
        )

        role.next_to(underline, DOWN, buff=0.3)

        self.play(
            FadeIn(role),
            run_time=0.8
        )

        self.wait(1)


        # =========================================================
        # 3. ABOUT ME
        # =========================================================

        self.play(
            FadeOut(name),
            FadeOut(underline),
            FadeOut(role),
            run_time=0.7
        )

        about_title = Text(
            "About Me",
            font_size=48,
            color=BLUE_B,
        )

        about_title.to_edge(UP)

        self.play(
            Write(about_title),
            run_time=0.8
        )

        about_group = VGroup()

        for item in ABOUT:
            text = Text(
                item,
                font_size=32,
                color=WHITE,
            )

            about_group.add(text)

        about_group.arrange(
            DOWN,
            aligned_edge=LEFT,
            buff=0.35
        )

        self.play(
            LaggedStart(
                *[
                    FadeIn(x, shift=RIGHT * 0.5)
                    for x in about_group
                ],
                lag_ratio=0.25
            ),
            run_time=2
        )

        self.wait(1)


        # =========================================================
        # 4. SKILLS
        # =========================================================

        self.play(
            FadeOut(about_title),
            FadeOut(about_group),
            run_time=0.7
        )

        skills_title = Text(
            "Tech Stack",
            font_size=48,
            color=GREEN_B,
        )

        skills_title.to_edge(UP)

        self.play(
            Write(skills_title),
            run_time=0.8
        )


        # Create skill cards
        skill_objects = []

        for skill in SKILLS:

            box = RoundedRectangle(
                width=3.2,
                height=0.7,
                corner_radius=0.15,
                stroke_color=GREEN_B,
                stroke_width=2,
                fill_color="#161B22",
                fill_opacity=1,
            )

            label = Text(
                skill,
                font_size=27,
                color=WHITE,
            )

            label.move_to(box)

            card = VGroup(box, label)

            skill_objects.append(card)


        skills_group = VGroup(*skill_objects)

        skills_group.arrange_in_grid(
            rows=2,
            cols=3,
            buff=0.35
        )

        self.play(
            LaggedStart(
                *[
                    FadeIn(card, scale=0.8)
                    for card in skills_group
                ],
                lag_ratio=0.15
            ),
            run_time=2
        )

        self.wait(1)


        # =========================================================
        # 5. GITHUB TERMINAL
        # =========================================================

        self.play(
            FadeOut(skills_title),
            FadeOut(skills_group),
            run_time=0.7
        )

        terminal = RoundedRectangle(
            width=10,
            height=4.8,
            corner_radius=0.2,
            stroke_color="#30363D",
            stroke_width=2,
            fill_color="#010409",
            fill_opacity=1,
        )

        self.play(
            FadeIn(terminal, scale=0.9),
            run_time=0.8
        )


        # Terminal header
        dot1 = Dot(
            point=terminal.get_corner(UL) + RIGHT * 0.35 + DOWN * 0.35,
            radius=0.07,
            color=RED_B
        )

        dot2 = Dot(
            point=terminal.get_corner(UL) + RIGHT * 0.65 + DOWN * 0.35,
            radius=0.07,
            color=YELLOW
        )

        dot3 = Dot(
            point=terminal.get_corner(UL) + RIGHT * 0.95 + DOWN * 0.35,
            radius=0.07,
            color=GREEN_B
        )

        self.play(
            FadeIn(dot1),
            FadeIn(dot2),
            FadeIn(dot3),
        )


        # Terminal text
        command = Text(
            "$ git status",
            font_size=28,
            font="DejaVu Sans Mono",
            color=GREEN_B,
        )

        command.move_to(
            terminal.get_center() + UP * 0.8
        )

        self.play(
            Write(command),
            run_time=1
        )


        output = Text(
            "✓ Everything is up to date",
            font_size=27,
            font="DejaVu Sans Mono",
            color=WHITE,
        )

        output.next_to(
            command,
            DOWN,
            aligned_edge=LEFT,
            buff=0.4
        )

        self.play(
            Write(output),
            run_time=1
        )


        command2 = Text(
            "$ git push origin main",
            font_size=28,
            font="DejaVu Sans Mono",
            color=GREEN_B,
        )

        command2.next_to(
            output,
            DOWN,
            aligned_edge=LEFT,
            buff=0.5
        )

        self.play(
            Write(command2),
            run_time=1
        )


        success = Text(
            "✓ Successfully pushed!",
            font_size=27,
            font="DejaVu Sans Mono",
            color=GREEN_B,
        )

        success.next_to(
            command2,
            DOWN,
            aligned_edge=LEFT,
            buff=0.4
        )

        self.play(
            Write(success),
            run_time=1
        )

        self.wait(1)


        # =========================================================
        # 6. FINAL PROFILE CARD
        # =========================================================

        self.play(
            FadeOut(
                VGroup(
                    terminal,
                    dot1,
                    dot2,
                    dot3,
                    command,
                    output,
                    command2,
                    success
                )
            ),
            run_time=0.8
        )


        final_name = Text(
            NAME,
            font_size=64,
            color=BLUE_B,
        )

        final_role = Text(
            ROLE,
            font_size=28,
            color=GREY_B,
        )

        github = Text(
            GITHUB,
            font_size=30,
            color=GREEN_B,
        )


        final_group = VGroup(
            final_name,
            final_role,
            github,
        )

        final_group.arrange(
            DOWN,
            buff=0.3
        )


        # Decorative circles
        circle1 = Circle(
            radius=2.5,
            stroke_color=BLUE_B,
            stroke_width=2,
        )

        circle2 = Circle(
            radius=2.8,
            stroke_color=GREEN_B,
            stroke_width=1,
        )

        circle1.move_to(final_group.get_center())
        circle2.move_to(final_group.get_center())


        self.play(
            Create(circle2),
            Create(circle1),
            run_time=1.2
        )

        self.play(
            FadeIn(
                final_group,
                shift=UP * 0.3
            ),
            run_time=1.2
        )

        self.wait(2)


        # =========================================================
        # 7. OUTRO
        # =========================================================

        self.play(
            final_group.animate.scale(0.8),
            circle1.animate.scale(0.8),
            circle2.animate.scale(0.8),
            run_time=0.8
        )

        thank_you = Text(
            "Thanks for visiting! ⭐",
            font_size=34,
            color=YELLOW,
        )

        thank_you.next_to(
            final_group,
            DOWN,
            buff=0.5
        )

        self.play(
            Write(thank_you),
            run_time=1
        )

        self.wait(2)

        self.play(
            FadeOut(
                VGroup(
                    final_group,
                    circle1,
                    circle2,
                    thank_you
                )
            ),
            run_time=1
        )
```


