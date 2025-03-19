from factory import Factory, Faker

class ProductFactory(Factory):
    class Meta:
        model = dict  # Using a dictionary to simulate a product model

    id = Faker('uuid4')
    name = Faker('word')
    category = Faker('word')
    available = Faker('boolean')
    price = Faker('random_number', digits=5)
