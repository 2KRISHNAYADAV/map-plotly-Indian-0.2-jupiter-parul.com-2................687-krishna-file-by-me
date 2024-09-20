# map-plotly-Indian-0.2-jupiter-parul.com-2................687-krishna-file-by-me


<body>

<h1>Jupyter Notebook Code</h1>


<code>
# Importing required libraries
import plotly.graph_objs as go
import numpy as np

# Defining latitude and longitude
lat = 22.2973142
lon = 73.1942567

# Creating the scatter plot
fig = go.Figure(go.Scattergeo(
    lat=[lat],
    lon=[lon],
    mode='markers',
    marker_color='red',
    marker_size=10,
))

# Updating layout to center the map and add properties
fig.update_layout(
    width=1000, height=800,
    geo=dict(
        center_lon=lon,
        center_lat=lat,
        projection_rotation_lon=lon,
        projection_rotation_lat=lat,
        showland=True,
        showcountries=True,
        landcolor='#99BBFF',
        countrycolor='#000000'
    )
)

# Showing the figure
fig.show()
</code>
</div>

<h2>Output</h2>
   
<div class="output-section">
    <img src="https://github.com/user-attachments/assets/25825120-e940-4ae2-a4c7-6c6bd074b0b5" alt="Screenshot 2024-09-20 134451" style="max-width: 100%;">
</div>

<h2>Sphere Earth Visualization   projectiontype='orthographic</h2>

<div class="code-section">
<code>
# Defining latitude and longitude
lat = 22.2973142
lon = 73.1942567

# Creating the scatter plot
fig = go.Figure(go.Scattergeo(
    lat=[lat],
    lon=[lon],
    mode='markers',
    marker=dict(
        color='red',
        size=10
    ),
))

# Updating layout to center the map and add properties
fig.update_layout(
    width=600, height=600,
    geo=dict(
        projection_type='orthographic',
        center=dict(lat=lat, lon=lon),
        projection=dict(rotation=dict(lon=lon)),
        projection_scale=0.9,
        showland=True,
        showcountries=True,
        landcolor='#99BBFF',
        countrycolor='#000000'
    )
)

# Showing the figure
fig.show()
</code>
</div>

<h2>Output</h2>

 <img src="https://github.com/user-attachments/assets/d0cfffc3-9477-497c-98a2-c30b835ddaae" alt="Screenshot 2024-09-20 140002" style="max-width: 100%;">


<h1> Albers Projection </h1>


<img src="https://github.com/user-attachments/assets/2b8fd676-698b-4572-ae4c-f537763b4d0d" alt="Screenshot 2024-09-20 140131" style="max-width: 100%;">


<h2> Output</h2>

 <img src="https://github.com/user-attachments/assets/67dde7b7-0245-45ab-8f36-1971588bd36d" alt="Screenshot 2024-09-20 140147" style="max-width: 100%;">


<CODE>

<H1>Animation on 🌎ROTATING<H1> 

import plotly.graph_objects as go
import numpy as np

# Define latitude and longitude
lat = 22.2973142
lon = 73.1942567

# Create a scatter plot
fig = go.Figure(go.Scattergeo(
    lat=[lat],
    lon=[lon],
    mode='markers',
    marker=dict(color='red', size=10)
))

#  layout with geographical properties
fig.update_layout(
    width=600,
    height=600,
    geo=dict(
        projection_type='orthographic',
        center=dict(lat=lat, lon=lon),
        projection_rotation=dict(lat=lat, lon=lon),
        projection_scale=0.9,
        showland=True,
        showcountries=True,
        landcolor='#99BBFF',
        countrycolor='#000000'
    ),
    updatemenus=[
        dict(
            type='buttons',
            showactive=False,
            y=1,
            x=1,
            xanchor='right',
            yanchor='top',
            pad=dict(t=0, r=10),
            buttons=[
                dict(
                    label='Rotating Btn',
                    method='animate',
                    args=[
                        None,
                        dict(
                            frame=dict(duration=20, redraw=True),
                            transition=dict(duration=0),
                            fromcurrent=True,
                            mode='immediate'
                        )
                    ]
                )
            ]
        )
    ]
)

#  frames for rotation animation
lon_range = np.arange(lon, 360 + lon, 2)
frames = [
    go.Frame(
        layout=dict(
            geo=dict(
                center=dict(lon=l),
                projection_rotation=dict(lon=l)
            )
        )
    ) for l in lon_range
]

#  frames in the figure
fig.update(frames=frames)

# Show the figure
fig.show()






  
<H2>OUTPUT</H2>
  

https://github.com/user-attachments/assets/debeb838-77ca-4f5b-879a-16a59e7b450f







<h1> More JN code on this JN Repository<h1>
<p>There are many similar codes related to this topic Types of Map Projections. You can visit my Jupyter notebook to view and run them for a better understanding.</p>

<h1>Types of Map Projections</h1>

<ul>
    <li>Natural Cat Shape Earth</li>
    <li>Aitoff Projection</li>
    <li>Flat Polar Quartic Projection</li>
    <li>Nell-Hammer Projection</li>
    <li>Satellite View</li>
    <li>Orthographic Projection for a 3D-like Globe</li>
    <li>Orthographic View: Flight Position</li>
    <li>Orthographic View: Vadodara (Gujarat) and Mumbai</li>
    <li>Conic Conformal Projection</li>
    <li>Foucaut Sinusoidal Projection</li>
    <li>And more...</li>
</ul>

  <CODE>

</body>
</html>
