EDA-Fall2023
ENV872 - Environmental Data Exploration - Fall 2023
Queenie Wei
Install and load the required package
heart_shape <- function(t) {
  x = 16 * sin(t)^3
  y = 13 * cos(t) - 5 * cos(2*t) - 2 * cos(3*t) - cos(4*t)
  return(data.frame(x, y))
}

# Generate points for the heart shape
t_values <- seq(0, 2 * pi, length.out = 1000)
heart_points <- heart_shape(t_values)

# Create the heart plot using ggplot2
heart_plot <- ggplot(heart_points, aes(x, y)) +
  geom_path(color = "red", size = 1) +
  coord_fixed(ratio = 1) +
  theme_void()

# Display the heart plot
print(heart_plot)
### Citation: ChatGPT Prompt: write codes that would draw a heart in R ####

