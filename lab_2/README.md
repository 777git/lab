============================= test session starts ==============================
platform linux -- Python 3.7.3, pytest-6.2.1, py-1.10.0, pluggy-0.13.1
rootdir: /home/user/lab/lab_2
collected 5 items

tests/tests.py ...F.                                                     [100%]

=================================== FAILURES ===================================
____________________________ TestClass.test_my_fun _____________________________

self = <tests.tests.TestClass testMethod=test_my_fun>

    def test_my_fun(self):
>       self.assertEqual(my_good_fun(), "Success")
E       AssertionError: 'success' != 'Success'
E       - success
E       ? ^
E       + Success
E       ? ^

tests/tests.py:29: AssertionError
=========================== short test summary info ============================
FAILED tests/tests.py::TestClass::test_my_fun - AssertionError: 'success' != ...
========================= 1 failed, 4 passed in 0.57s ==========================
