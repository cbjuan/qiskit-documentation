# qiskit.circuit.library.CRZGate

<span id="undefined" />

`CRZGate(theta, label=None, ctrl_state=None)`

Controlled-RZ gate.

This is a diagonal but non-symmetric gate that induces a phase on the state of the target qubit, depending on the control state.

**Circuit symbol:**

```python
q_0: ────■────
     ┌───┴───┐
q_1: ┤ Rz(λ) ├
     └───────┘
```

**Matrix representation:**

$$
\begin{split}CRZ(\lambda)\ q_0, q_1 =
    I \otimes |0\rangle\langle 0| + RZ(\lambda) \otimes |1\rangle\langle 1| =
    \begin{pmatrix}
        1 & 0 & 0 & 0 \\
        0 & e^{-i\frac{\lambda}{2}} & 0 & 0 \\
        0 & 0 & 1 & 0 \\
        0 & 0 & 0 & e^{i\frac{\lambda}{2}}
    \end{pmatrix}\end{split}
$$

<Admonition title="Note" type="note">
  In Qiskit’s convention, higher qubit indices are more significant (little endian convention). In many textbooks, controlled gates are presented with the assumption of more significant qubits as control, which in our case would be q\_1. Thus a textbook matrix for this gate will be:

  ```python
       ┌───────┐
  q_0: ┤ Rz(λ) ├
       └───┬───┘
  q_1: ────■────
  ```

  $$
  \begin{split}CRZ(\lambda)\ q_1, q_0 =
      |0\rangle\langle 0| \otimes I + |1\rangle\langle 1| \otimes RZ(\lambda) =
      \begin{pmatrix}
          1 & 0 & 0 & 0 \\
          0 & 1 & 0 & 0 \\
          0 & 0 & e^{-i\frac{\lambda}{2}} & 0 \\
          0 & 0 & 0 & e^{i\frac{\lambda}{2}}
      \end{pmatrix}\end{split}
  $$
</Admonition>

<Admonition title="See also" type="note">
  `CU1Gate`: Due to the global phase difference in the matrix definitions of U1 and RZ, CU1 and CRZ are different gates with a relative phase difference.
</Admonition>

Create new CRZ gate.

<span id="undefined" />

`__init__(theta, label=None, ctrl_state=None)`

Create new CRZ gate.

## Methods

|                                                                                                                                                 |                                                                          |
| ----------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------ |
| [`__init__`](#qiskit.circuit.library.CRZGate.__init__ "qiskit.circuit.library.CRZGate.__init__")(theta\[, label, ctrl\_state])                  | Create new CRZ gate.                                                     |
| [`add_decomposition`](#qiskit.circuit.library.CRZGate.add_decomposition "qiskit.circuit.library.CRZGate.add_decomposition")(decomposition)      | Add a decomposition of the instruction to the SessionEquivalenceLibrary. |
| [`assemble`](#qiskit.circuit.library.CRZGate.assemble "qiskit.circuit.library.CRZGate.assemble")()                                              | Assemble a QasmQobjInstruction                                           |
| [`broadcast_arguments`](#qiskit.circuit.library.CRZGate.broadcast_arguments "qiskit.circuit.library.CRZGate.broadcast_arguments")(qargs, cargs) | Validation and handling of the arguments and its relationship.           |
| [`c_if`](#qiskit.circuit.library.CRZGate.c_if "qiskit.circuit.library.CRZGate.c_if")(classical, val)                                            | Add classical condition on register classical and value val.             |
| [`control`](#qiskit.circuit.library.CRZGate.control "qiskit.circuit.library.CRZGate.control")(\[num\_ctrl\_qubits, label, ctrl\_state])         | Return controlled version of gate.                                       |
| [`copy`](#qiskit.circuit.library.CRZGate.copy "qiskit.circuit.library.CRZGate.copy")(\[name])                                                   | Copy of the instruction.                                                 |
| [`inverse`](#qiskit.circuit.library.CRZGate.inverse "qiskit.circuit.library.CRZGate.inverse")()                                                 | Return inverse CRZ gate (i.e.                                            |
| [`is_parameterized`](#qiskit.circuit.library.CRZGate.is_parameterized "qiskit.circuit.library.CRZGate.is_parameterized")()                      | Return True .IFF.                                                        |
| [`mirror`](#qiskit.circuit.library.CRZGate.mirror "qiskit.circuit.library.CRZGate.mirror")()                                                    | DEPRECATED: use instruction.reverse\_ops().                              |
| [`power`](#qiskit.circuit.library.CRZGate.power "qiskit.circuit.library.CRZGate.power")(exponent)                                               | Creates a unitary gate as gate^exponent.                                 |
| [`qasm`](#qiskit.circuit.library.CRZGate.qasm "qiskit.circuit.library.CRZGate.qasm")()                                                          | Return a default OpenQASM string for the instruction.                    |
| [`repeat`](#qiskit.circuit.library.CRZGate.repeat "qiskit.circuit.library.CRZGate.repeat")(n)                                                   | Creates an instruction with gate repeated n amount of times.             |
| [`reverse_ops`](#qiskit.circuit.library.CRZGate.reverse_ops "qiskit.circuit.library.CRZGate.reverse_ops")()                                     | For a composite instruction, reverse the order of sub-instructions.      |
| [`soft_compare`](#qiskit.circuit.library.CRZGate.soft_compare "qiskit.circuit.library.CRZGate.soft_compare")(other)                             | Soft comparison between gates.                                           |
| [`to_matrix`](#qiskit.circuit.library.CRZGate.to_matrix "qiskit.circuit.library.CRZGate.to_matrix")()                                           | Return a Numpy.array for the gate unitary matrix.                        |
| [`validate_parameter`](#qiskit.circuit.library.CRZGate.validate_parameter "qiskit.circuit.library.CRZGate.validate_parameter")(parameter)       | Gate parameters should be int, float, or ParameterExpression             |

## Attributes

|                                                                                                                       |                                                                               |
| --------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------- |
| [`ctrl_state`](#qiskit.circuit.library.CRZGate.ctrl_state "qiskit.circuit.library.CRZGate.ctrl_state")                | Return the control state of the gate as a decimal integer.                    |
| [`decompositions`](#qiskit.circuit.library.CRZGate.decompositions "qiskit.circuit.library.CRZGate.decompositions")    | Get the decompositions of the instruction from the SessionEquivalenceLibrary. |
| [`definition`](#qiskit.circuit.library.CRZGate.definition "qiskit.circuit.library.CRZGate.definition")                | Return definition in terms of other basic gates.                              |
| [`duration`](#qiskit.circuit.library.CRZGate.duration "qiskit.circuit.library.CRZGate.duration")                      | Get the duration.                                                             |
| [`label`](#qiskit.circuit.library.CRZGate.label "qiskit.circuit.library.CRZGate.label")                               | Return gate label                                                             |
| [`name`](#qiskit.circuit.library.CRZGate.name "qiskit.circuit.library.CRZGate.name")                                  | Get name of gate.                                                             |
| [`num_ctrl_qubits`](#qiskit.circuit.library.CRZGate.num_ctrl_qubits "qiskit.circuit.library.CRZGate.num_ctrl_qubits") | Get number of control qubits.                                                 |
| [`params`](#qiskit.circuit.library.CRZGate.params "qiskit.circuit.library.CRZGate.params")                            | Get parameters from base\_gate.                                               |
| [`unit`](#qiskit.circuit.library.CRZGate.unit "qiskit.circuit.library.CRZGate.unit")                                  | Get the time unit of duration.                                                |

<span id="undefined" />

`add_decomposition(decomposition)`

Add a decomposition of the instruction to the SessionEquivalenceLibrary.

<span id="undefined" />

`assemble()`

Assemble a QasmQobjInstruction

**Return type**

`Instruction`

<span id="undefined" />

`broadcast_arguments(qargs, cargs)`

Validation and handling of the arguments and its relationship.

For example, `cx([q[0],q[1]], q[2])` means `cx(q[0], q[2]); cx(q[1], q[2])`. This method yields the arguments in the right grouping. In the given example:

```python
in: [[q[0],q[1]], q[2]],[]
outs: [q[0], q[2]], []
      [q[1], q[2]], []
```

The general broadcasting rules are:

> *   If len(qargs) == 1:
>
>     ```python
>     [q[0], q[1]] -> [q[0]],[q[1]]
>     ```
>
> *   If len(qargs) == 2:
>
>     ```python
>     [[q[0], q[1]], [r[0], r[1]]] -> [q[0], r[0]], [q[1], r[1]]
>     [[q[0]], [r[0], r[1]]]       -> [q[0], r[0]], [q[0], r[1]]
>     [[q[0], q[1]], [r[0]]]       -> [q[0], r[0]], [q[1], r[0]]
>     ```
>
> *   If len(qargs) >= 3:
>
>     ```python
>     [q[0], q[1]], [r[0], r[1]],  ...] -> [q[0], r[0], ...], [q[1], r[1], ...]
>     ```

**Parameters**

*   **qargs** (`List`) – List of quantum bit arguments.
*   **cargs** (`List`) – List of classical bit arguments.

**Return type**

`Tuple`\[`List`, `List`]

**Returns**

A tuple with single arguments.

**Raises**

**CircuitError** – If the input is not valid. For example, the number of arguments does not match the gate expectation.

<span id="undefined" />

`c_if(classical, val)`

Add classical condition on register classical and value val.

<span id="undefined" />

`control(num_ctrl_qubits=1, label=None, ctrl_state=None)`

Return controlled version of gate. See [`ControlledGate`](qiskit.circuit.ControlledGate#qiskit.circuit.ControlledGate "qiskit.circuit.ControlledGate") for usage.

**Parameters**

*   **num\_ctrl\_qubits** (`Optional`\[`int`]) – number of controls to add to gate (default=1)
*   **label** (`Optional`\[`str`]) – optional gate label
*   **ctrl\_state** (`Union`\[`int`, `str`, `None`]) – The control state in decimal or as a bitstring (e.g. ‘111’). If None, use 2\*\*num\_ctrl\_qubits-1.

**Returns**

Controlled version of gate. This default algorithm uses num\_ctrl\_qubits-1 ancillae qubits so returns a gate of size num\_qubits + 2\*num\_ctrl\_qubits - 1.

**Return type**

[qiskit.circuit.ControlledGate](qiskit.circuit.ControlledGate#qiskit.circuit.ControlledGate "qiskit.circuit.ControlledGate")

**Raises**

**QiskitError** – unrecognized mode or invalid ctrl\_state

<span id="undefined" />

`copy(name=None)`

Copy of the instruction.

**Parameters**

**name** (*str*) – name to be given to the copied circuit, if None then the name stays the same.

**Returns**

**a copy of the current instruction, with the name**

updated if it was provided

**Return type**

[qiskit.circuit.Instruction](qiskit.circuit.Instruction#qiskit.circuit.Instruction "qiskit.circuit.Instruction")

<span id="undefined" />

`property ctrl_state`

Return the control state of the gate as a decimal integer.

**Return type**

`int`

<span id="undefined" />

`property decompositions`

Get the decompositions of the instruction from the SessionEquivalenceLibrary.

<span id="undefined" />

`property definition`

Return definition in terms of other basic gates. If the gate has open controls, as determined from self.ctrl\_state, the returned definition is conjugated with X without changing the internal \_definition.

**Return type**

`List`

<span id="undefined" />

`property duration`

Get the duration.

<span id="undefined" />

`inverse()`

Return inverse CRZ gate (i.e. with the negative rotation angle).

<span id="undefined" />

`is_parameterized()`

Return True .IFF. instruction is parameterized else False

<span id="undefined" />

`property label`

Return gate label

**Return type**

`str`

<span id="undefined" />

`mirror()`

DEPRECATED: use instruction.reverse\_ops().

**Returns**

**a new instruction with sub-instructions**

reversed.

**Return type**

[qiskit.circuit.Instruction](qiskit.circuit.Instruction#qiskit.circuit.Instruction "qiskit.circuit.Instruction")

<span id="undefined" />

`property name`

Get name of gate. If the gate has open controls the gate name will become:

> \<original\_name\_o\<ctrl\_state>

where \<original\_name> is the gate name for the default case of closed control qubits and \<ctrl\_state> is the integer value of the control state for the gate.

**Return type**

`str`

<span id="undefined" />

`property num_ctrl_qubits`

Get number of control qubits.

**Returns**

The number of control qubits for the gate.

**Return type**

int

<span id="undefined" />

`property params`

Get parameters from base\_gate.

**Returns**

List of gate parameters.

**Return type**

list

**Raises**

**CircuitError** – Controlled gate does not define a base gate

<span id="undefined" />

`power(exponent)`

Creates a unitary gate as gate^exponent.

**Parameters**

**exponent** (*float*) – Gate^exponent

**Returns**

To which to\_matrix is self.to\_matrix^exponent.

**Return type**

[qiskit.extensions.UnitaryGate](qiskit.extensions.UnitaryGate#qiskit.extensions.UnitaryGate "qiskit.extensions.UnitaryGate")

**Raises**

**CircuitError** – If Gate is not unitary

<span id="undefined" />

`qasm()`

Return a default OpenQASM string for the instruction.

Derived instructions may override this to print in a different format (e.g. measure q\[0] -> c\[0];).

<span id="undefined" />

`repeat(n)`

Creates an instruction with gate repeated n amount of times.

**Parameters**

**n** (*int*) – Number of times to repeat the instruction

**Returns**

Containing the definition.

**Return type**

[qiskit.circuit.Instruction](qiskit.circuit.Instruction#qiskit.circuit.Instruction "qiskit.circuit.Instruction")

**Raises**

**CircuitError** – If n \< 1.

<span id="undefined" />

`reverse_ops()`

For a composite instruction, reverse the order of sub-instructions.

This is done by recursively reversing all sub-instructions. It does not invert any gate.

**Returns**

**a new instruction with**

sub-instructions reversed.

**Return type**

[qiskit.circuit.Instruction](qiskit.circuit.Instruction#qiskit.circuit.Instruction "qiskit.circuit.Instruction")

<span id="undefined" />

`soft_compare(other)`

Soft comparison between gates. Their names, number of qubits, and classical bit numbers must match. The number of parameters must match. Each parameter is compared. If one is a ParameterExpression then it is not taken into account.

**Parameters**

**other** (*instruction*) – other instruction.

**Returns**

are self and other equal up to parameter expressions.

**Return type**

bool

<span id="undefined" />

`to_matrix()`

Return a Numpy.array for the gate unitary matrix.

**Returns**

if the Gate subclass has a matrix definition.

**Return type**

np.ndarray

**Raises**

**CircuitError** – If a Gate subclass does not implement this method an exception will be raised when this base class method is called.

<span id="undefined" />

`property unit`

Get the time unit of duration.

<span id="undefined" />

`validate_parameter(parameter)`

Gate parameters should be int, float, or ParameterExpression