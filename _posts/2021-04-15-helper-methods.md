1) Refactored Routes:
Rails.application.routes.draw do
  # get "/", controller: "movies", action: "index" 
  # get "/" => "movies#index" 
  root "movies#index

2) Terminal:
rails routes

OR on web browser
https://3000-amber-sawfish-27b1cyxf.ws-us03.gitpod.io/**rails/info/routes**


3) name your URLs from now on for better defense coding:
# READ
  get "/movies" => "movies#index"
  get "/movies/:id" => "movies#show", as: :details
  
 on the index.html.erb (for movies template):
 <h2>
  <%= details_url(42) %>
</h2>

4) From now on, no longer writing out raw a href links:

  <a href="<%=new_movies_path%>">Add a new movie</a>
  
 We are going to use helper method link_to:

<%= link_to "Add a new movie", new_movies_path%>


Part 2:

1) <%= form_with(url: movies_path) do %>
    <%end%>
    
    Automatically gives us authenticity token, don't have to worry about it!
    Replaces App Dev 1:
    
    <form action="<%= movies_path%>" method="post">
    <input name="authenticity_token" value="<%= form_authenticity_token %>" type="hidden">
    
 
