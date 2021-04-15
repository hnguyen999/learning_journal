1) Refactored Routes:
Rails.application.routes.draw do
  # get "/", controller: "movies", action: "index" 
  # get "/" => "movies#index" 
  root "movies#index

2) Terminal:
rails routes

OR on web browser
https://3000-amber-sawfish-27b1cyxf.ws-us03.gitpod.io/****rails/**info/routes******
