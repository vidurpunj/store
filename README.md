# README
Migrations:
rails g model Product name 'price:decimal{12,3}' active:boolean\n
rails g model OrderStatus name:string
rails g model Order 'subtotal:decimal{12,3}' 'tax:decimal{12,3}' 'shipping:decimal{12,3}' 'total:decimal{12,3}' order_status:references
rails g model OrderItem product:references order:references 'unit_price:decimal{12,3}' quantity:integer 'total_price:decimal{12,3}'
rake db:migrate
rake db:seed
