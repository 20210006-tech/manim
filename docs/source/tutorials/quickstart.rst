from manim import *
import random

class UltraInstinctExponential(Scene):
    def construct(self):

        # -------------------------
        # Cosmic Background
        # -------------------------
        bg = Rectangle(width=14, height=8, fill_color=BLACK, fill_opacity=1)
        self.add(bg)

        stars = VGroup(*[
            Dot(point=[random.uniform(-7,7), random.uniform(-4,4),0],
                radius=0.02, color=WHITE)
            for _ in range(120)
        ])
        self.add(stars)

        # -------------------------
        # Calm Intro
        # -------------------------
        intro = Text("I have reached Ultra Instinct...", 
                     font_size=40, color=GRAY_A)
        self.play(FadeIn(intro))
        self.wait(2)

        self.play(FadeOut(intro))

        # -------------------------
        # Transformation Flash
        # -------------------------
        flash = Rectangle(width=14, height=8,
                          fill_color=WHITE,
                          fill_opacity=1)
        self.play(FadeIn(flash), run_time=0.2)
        self.play(FadeOut(flash), run_time=0.4)

        # Aura
        aura = Circle(radius=3, color=BLUE)
        aura.set_fill(BLUE_E, opacity=0.15)
        self.play(GrowFromCenter(aura))
        self.wait(1)

        title = Text("ULTRA INSTINCT EXPONENTIAL POWER",
                     font_size=42, color=GRAY_B)
        self.play(Write(title))
        self.wait(2)
        self.play(FadeOut(title))

        # -------------------------
        # Formula with Glow Effect
        # -------------------------
        formula = MathTex("f(x) = a \\cdot b^x", font_size=72)
        formula.set_color(WHITE)

        glow = SurroundingRectangle(formula,
                                     color=BLUE,
                                     buff=0.3)
        glow.set_stroke(width=6)

        self.play(Write(formula))
        self.play(Create(glow))
        self.wait(2)

        explain1 = Text("a = Initial Power Level",
                        font_size=30).next_to(formula, DOWN)
        explain2 = Text("b = Energy Multiplier",
                        font_size=30).next_to(explain1, DOWN)

        self.play(Write(explain1), Write(explain2))
        self.wait(3)

        self.play(FadeOut(formula),
                  FadeOut(glow),
                  FadeOut(explain1),
                  FadeOut(explain2))

        # -------------------------
        # Graph Section
        # -------------------------
        axes = Axes(
            x_range=[-4,4,1],
            y_range=[0,10,2],
            axis_config={"include_numbers": True},
        )

        labels = axes.get_axis_labels("x","y")

        self.play(Create(axes), Write(labels))

        # Growth
        growth = axes.plot(lambda x: 2**x)
        growth_label = Text("Growth (b > 1)",
                            font_size=30).to_edge(UP)

        self.play(Create(growth), Write(growth_label))
        self.wait(3)

        # Smooth Transform to Decay
        decay = axes.plot(lambda x: (0.5)**x)
        decay_label = Text("Decay (0 < b < 1)",
                           font_size=30).to_edge(UP)

        self.play(Transform(growth, decay),
                  Transform(growth_label, decay_label))
        self.wait(3)

        # Domain & Range
        domain = Text("Domain: All real numbers",
                      font_size=30).to_edge(LEFT)
        range_text = Text("Range: y > 0",
                          font_size=30).next_to(domain, DOWN)

        self.play(Write(domain), Write(range_text))
        self.wait(3)

        # Y-Intercept
        y_dot = Dot(axes.c2p(0,1), radius=0.08)
        y_text = Text("Y-Intercept = a",
                      font_size=28).to_edge(RIGHT)

        self.play(Create(y_dot), Write(y_text))
        self.wait(3)

        # Asymptote
        asymptote = DashedLine(
            axes.c2p(-4,0),
            axes.c2p(4,0)
        )
        asym_text = Text("Horizontal Asymptote: y = 0",
                         font_size=28).to_edge(DOWN)

        self.play(Create(asymptote), Write(asym_text))
        self.wait(3)

        # -------------------------
        # Camera Shake Finale
        # -------------------------
        self.play(FadeOut(*self.mobjects))

        final = Text("EXPONENTIAL POWER LEVEL...",
                     font_size=48)
        self.play(Write(final))
        self.wait(2)

        over9000 = Text("IT'S OVER 9000!!!",
                        font_size=60)
        self.play(Transform(final, over9000),
                  run_time=1.5,
                  rate_func=there_and_back)
        self.wait(3)from manim import *
import random

class UltraInstinctExponential(Scene):
    def construct(self):

        # -------------------------
        # Cosmic Background
        # -------------------------
        bg = Rectangle(width=14, height=8, fill_color=BLACK, fill_opacity=1)
        self.add(bg)

        stars = VGroup(*[
            Dot(point=[random.uniform(-7,7), random.uniform(-4,4),0],
                radius=0.02, color=WHITE)
            for _ in range(120)
        ])
        self.add(stars)

        # -------------------------
        # Calm Intro
        # -------------------------
        intro = Text("I have reached Ultra Instinct...", 
                     font_size=40, color=GRAY_A)
        self.play(FadeIn(intro))
        self.wait(2)

        self.play(FadeOut(intro))

        # -------------------------
        # Transformation Flash
        # -------------------------
        flash = Rectangle(width=14, height=8,
                          fill_color=WHITE,
                          fill_opacity=1)
        self.play(FadeIn(flash), run_time=0.2)
        self.play(FadeOut(flash), run_time=0.4)

        # Aura
        aura = Circle(radius=3, color=BLUE)
        aura.set_fill(BLUE_E, opacity=0.15)
        self.play(GrowFromCenter(aura))
        self.wait(1)

        title = Text("ULTRA INSTINCT EXPONENTIAL POWER",
                     font_size=42, color=GRAY_B)
        self.play(Write(title))
        self.wait(2)
        self.play(FadeOut(title))

        # -------------------------
        # Formula with Glow Effect
        # -------------------------
        formula = MathTex("f(x) = a \\cdot b^x", font_size=72)
        formula.set_color(WHITE)

        glow = SurroundingRectangle(formula,
                                     color=BLUE,
                                     buff=0.3)
        glow.set_stroke(width=6)

        self.play(Write(formula))
        self.play(Create(glow))
        self.wait(2)

        explain1 = Text("a = Initial Power Level",
                        font_size=30).next_to(formula, DOWN)
        explain2 = Text("b = Energy Multiplier",
                        font_size=30).next_to(explain1, DOWN)

        self.play(Write(explain1), Write(explain2))
        self.wait(3)

        self.play(FadeOut(formula),
                  FadeOut(glow),
                  FadeOut(explain1),
                  FadeOut(explain2))

        # -------------------------
        # Graph Section
        # -------------------------
        axes = Axes(
            x_range=[-4,4,1],
            y_range=[0,10,2],
            axis_config={"include_numbers": True},
        )

        labels = axes.get_axis_labels("x","y")

        self.play(Create(axes), Write(labels))

        # Growth
        growth = axes.plot(lambda x: 2**x)
        growth_label = Text("Growth (b > 1)",
                            font_size=30).to_edge(UP)

        self.play(Create(growth), Write(growth_label))
        self.wait(3)

        # Smooth Transform to Decay
        decay = axes.plot(lambda x: (0.5)**x)
        decay_label = Text("Decay (0 < b < 1)",
                           font_size=30).to_edge(UP)

        self.play(Transform(growth, decay),
                  Transform(growth_label, decay_label))
        self.wait(3)

        # Domain & Range
        domain = Text("Domain: All real numbers",
                      font_size=30).to_edge(LEFT)
        range_text = Text("Range: y > 0",
                          font_size=30).next_to(domain, DOWN)

        self.play(Write(domain), Write(range_text))
        self.wait(3)

        # Y-Intercept
        y_dot = Dot(axes.c2p(0,1), radius=0.08)
        y_text = Text("Y-Intercept = a",
                      font_size=28).to_edge(RIGHT)

        self.play(Create(y_dot), Write(y_text))
        self.wait(3)

        # Asymptote
        asymptote = DashedLine(
            axes.c2p(-4,0),
            axes.c2p(4,0)
        )
        asym_text = Text("Horizontal Asymptote: y = 0",
                         font_size=28).to_edge(DOWN)

        self.play(Create(asymptote), Write(asym_text))
        self.wait(3)

        # -------------------------
        # Camera Shake Finale
        # -------------------------
        self.play(FadeOut(*self.mobjects))

        final = Text("EXPONENTIAL POWER LEVEL...",
                     font_size=48)
        self.play(Write(final))
        self.wait(2)

        over9000 = Text("IT'S OVER 9000!!!",
                        font_size=60)
        self.play(Transform(final, over9000),
                  run_time=1.5,
                  rate_func=there_and_back)
        self.wait(3)
