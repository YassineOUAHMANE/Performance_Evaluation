# Graphics Critique

My critique of the graphics in the "Training" part of the course slides,
using the checklist for good graphics.

---

## 1. Total brand sales in Europe (Audi, BMW, Mercedes)
- Good: title, legend, only 3 curves, colours easy to tell apart.
- The y-axis starts at 400 000, not 0, so the differences look bigger than they are.
- No axis labels and no units (cars? euros?).
- No source.

## 2. Demandeurs d'emploi (Pôle emploi)
- Legend "A" and "ABC" is cryptic if you don't know the categories.
- The title says 1996 to 2017, but the graphic only shows about 2011 to 2017.
- The y-axis does not start at 0.
- The zoom button and the slider are useless on a printed graphic (too much ink).

## 3. Le chômage
- Two graphics in one, with different scales and units (people vs thousands).
- The y-axis starts at 1 800 000, so the rise looks huge.
- Too many annotations and boxes: hard to know where to look.
- The grey bands are not explained.

## 4. Sous-alimentation dans le monde
- Every point has its value written on it **and** there is an axis, so it says the same thing twice.
- Heavy vertical grid lines, tiny text.
- The y-axis starts at 600, not 0.
- The data is a 3-year average, so the points overlap in time; joining them suggests more precision than there is.

## 5. Juvenile drug arrests vs kids killed by their parent
- Two y-axes with different scales: you can make any two curves look related this way (a way to cheat).
- The smoothing invents values between the years (the curve goes below the real points).
- It suggests a link between two unrelated things.

## 6. XRP/EUR (Investing.com)
- No axis labels and no units, and the time axis (16, 12:00, 17) is cryptic.
- The logo, the "Market open" label and the price box are not useful information.
- OK for a trader, but not for a general reader.

## 7. Évolution du nombre de catastrophes naturelles
- Only one curve, simple and clear, and the source is given.
- No y-axis label: number of what? per year?
- The x-axis is irregular (1980, 1990, 2000, 2010, then 2017).
- The dark background is bad for printing.

## 8. Monthly number of objects in Earth orbit
- Good: title, legend, caption, 5 curves (fewer than 6), comparable on the same scale.
- Small, rotated labels, and a very dense grid.
- "Total" is the sum of the other curves, which is fine but should be said.

## 9. Temperature cooling scheme for different α
- Good: a caption, few curves.
- No axis labels and no units.
- The line styles (dotted, dashed) are hard to tell apart.
- What α means is not explained.

## 10. SA : 512-node grid
- 18 curves (far more than 6): impossible to read.
- Many similar colours, and the legend is bigger than the graphic.
- No axis labels.
- The cryptic notation "i:16 a:10" needs the caption to be understood.

## 11. Table 7 : Response time
- A table of numbers instead of a graphic, so it is hard to compare.
- The confidence intervals are huge (e.g. 1122 ± 2 648 874): the values mean nothing.
- The scientific notation (E4, E6) is hard to read, and no units are given.

## 12. Nombre moyen de clients en fonction de lambda
- Only 3 points per curve: not enough.
- Joining them with straight lines is wrong, because queues grow very fast near λ = 1.
- The legend lists 4 laws but only 3 curves are visible (one is hidden).
- There is green in the legend, and no confidence intervals.

## 13. Grey curves with a text legend
- The legend says red, blue, green, black, but all the curves look grey or pale: you can't tell them apart.
- The legend is plain text under the graphic instead of being on it.
- The axis labels are tiny and the graphic has no title.

## 14. Report page with small figures
- The figures are too small to read.
- The figures are put in the text without real captions or a link to it.

## 15. Temps de réponse en fonction de lambda
- Too many points (100 000): a cloud of colours, nothing readable.
- The colours have no legend.
- The y-label "Response(n, lambda, mu)" is cryptic.
- The title says "temps moyen" (mean), but the graphic shows every single value, not the mean.

## 16. Screen shots of each law
- Real screenshots: low quality and small.
- One graphic per law, with different scales, so you can't compare them.
- They should all be on the same graphic.

## 17. Simulation de file d'attente
- The best one: title, caption, labelled axes, legend, 5 curves on the same scale.
- Yellow and green are hard to see on white.
- The curves are cut at N = 20 with no explanation, and there are no confidence intervals.

## 18. Évolution de la file d'attente en fonction du débit
- 7 curves (more than 6), and several colours are too similar.
- The curves stop at different places, which is not explained.
- The x-axis goes to 1.2 but nothing happens after 1: wasted space.
- The labels are tiny, and the x-label is only "(λ)".
