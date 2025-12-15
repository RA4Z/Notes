To loop over two or more sequences at the same time in [[🐍Python]], the entries can be paired with the `zip()` function.
```Python
questions = ['name', 'quest', 'favorite color']
answers = ['lancelot', 'the holy grail', 'blue']
for q, a in zip(questions, answers):
    print('What is your {0}?  It is {1}.'.format(q, a))

# Output: gallahad the pure
# Output: robin the brave
```