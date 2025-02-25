## API Report File for "@moneyprotocol/lib-base"

> Do not edit this file. It is a report generated by [API Extractor](https://api-extractor.com/).

```ts

// @public
export const BPD_LIQUIDATION_RESERVE: Decimal;

// @public
export const BPD_MINIMUM_DEBT: Decimal;

// @public
export const BPD_MINIMUM_NET_DEBT: Decimal;

// @internal (undocumented)
export type _BPDBorrowing<T> = {
    borrowBPD: T;
};

// @internal (undocumented)
export type _BPDRepayment<T> = {
    repayBPD: T;
};

// @internal (undocumented)
export class _CachedReadableMoneyp<T extends unknown[]> implements _ReadableMoneypWithExtraParams<T> {
    constructor(readable: _ReadableMoneypWithExtraParams<T>, cache: _MoneypReadCache<T>);
    // (undocumented)
    getBPDBalance(address?: string, ...extraParams: T): Promise<Decimal>;
    // (undocumented)
    getBPDInStabilityPool(...extraParams: T): Promise<Decimal>;
    // (undocumented)
    getCollateralSurplusBalance(address?: string, ...extraParams: T): Promise<Decimal>;
    // (undocumented)
    getFees(...extraParams: T): Promise<Fees>;
    // (undocumented)
    getFrontendStatus(address?: string, ...extraParams: T): Promise<FrontendStatus>;
    // (undocumented)
    getLiquidityMiningMPReward(address?: string, ...extraParams: T): Promise<Decimal>;
    // (undocumented)
    getLiquidityMiningStake(address?: string, ...extraParams: T): Promise<Decimal>;
    // (undocumented)
    getMPBalance(address?: string, ...extraParams: T): Promise<Decimal>;
    // (undocumented)
    getMPStake(address?: string, ...extraParams: T): Promise<MPStake>;
    // (undocumented)
    getNumberOfVaults(...extraParams: T): Promise<number>;
    // (undocumented)
    getPrice(...extraParams: T): Promise<Decimal>;
    // (undocumented)
    getRemainingLiquidityMiningMPReward(...extraParams: T): Promise<Decimal>;
    // (undocumented)
    getRemainingStabilityPoolMPReward(...extraParams: T): Promise<Decimal>;
    // (undocumented)
    getRskSwapTokenAllowance(address?: string, ...extraParams: T): Promise<Decimal>;
    // (undocumented)
    getRskSwapTokenBalance(address?: string, ...extraParams: T): Promise<Decimal>;
    // (undocumented)
    getStabilityDeposit(address?: string, ...extraParams: T): Promise<StabilityDeposit>;
    // (undocumented)
    getTotal(...extraParams: T): Promise<Vault>;
    // (undocumented)
    getTotalRedistributed(...extraParams: T): Promise<Vault>;
    // (undocumented)
    getTotalStakedMP(...extraParams: T): Promise<Decimal>;
    // (undocumented)
    getTotalStakedRskSwapTokens(...extraParams: T): Promise<Decimal>;
    // (undocumented)
    getVault(address?: string, ...extraParams: T): Promise<UserVault>;
    // (undocumented)
    getVaultBeforeRedistribution(address?: string, ...extraParams: T): Promise<VaultWithPendingRedistribution>;
    // (undocumented)
    getVaults(params: VaultListingParams & {
        beforeRedistribution: true;
    }, ...extraParams: T): Promise<VaultWithPendingRedistribution[]>;
    // (undocumented)
    getVaults(params: VaultListingParams, ...extraParams: T): Promise<UserVault[]>;
    }

// @internal (undocumented)
export type _CollateralChange<T> = (_CollateralDeposit<T> & _NoCollateralWithdrawal) | (_CollateralWithdrawal<T> & _NoCollateralDeposit);

// @internal (undocumented)
export type _CollateralDeposit<T> = {
    depositCollateral: T;
};

// @public
export interface CollateralGainTransferDetails extends StabilityPoolGainsWithdrawalDetails {
    newVault: Vault;
}

// @internal (undocumented)
export type _CollateralWithdrawal<T> = {
    withdrawCollateral: T;
};

// @public
export const CRITICAL_COLLATERAL_RATIO: Decimal;

// @internal (undocumented)
export type _DebtChange<T> = (_BPDBorrowing<T> & _NoBPDRepayment) | (_BPDRepayment<T> & _NoBPDBorrowing);

// @public
export class Decimal {
    // @internal (undocumented)
    get absoluteValue(): this;
    // (undocumented)
    add(addend: Decimalish): Decimal;
    // @internal (undocumented)
    get bigNumber(): string;
    // (undocumented)
    div(divider: Decimalish): Decimal;
    // @internal (undocumented)
    _divCeil(divider: Decimalish): Decimal;
    // (undocumented)
    eq(that: Decimalish): boolean;
    // (undocumented)
    get finite(): this | undefined;
    // (undocumented)
    static from(decimalish: Decimalish): Decimal;
    // (undocumented)
    static fromBigNumberString(bigNumberString: string): Decimal;
    // (undocumented)
    gt(that: Decimalish): boolean;
    // (undocumented)
    gte(that: Decimalish): boolean;
    // (undocumented)
    static readonly HALF: Decimal;
    // @internal (undocumented)
    get hex(): string;
    // (undocumented)
    get infinite(): this | undefined;
    // (undocumented)
    static readonly INFINITY: Decimal;
    // (undocumented)
    get isZero(): boolean;
    // (undocumented)
    lt(that: Decimalish): boolean;
    // (undocumented)
    lte(that: Decimalish): boolean;
    // (undocumented)
    static max(a: Decimalish, b: Decimalish): Decimal;
    // (undocumented)
    static min(a: Decimalish, b: Decimalish): Decimal;
    // (undocumented)
    mul(multiplier: Decimalish): Decimal;
    // (undocumented)
    mulDiv(multiplier: Decimalish, divider: Decimalish): Decimal;
    // (undocumented)
    get nonZero(): this | undefined;
    // (undocumented)
    static readonly ONE: Decimal;
    // (undocumented)
    pow(exponent: number): Decimal;
    // (undocumented)
    prettify(precision?: number): string;
    // (undocumented)
    shorten(): string;
    // (undocumented)
    sub(subtrahend: Decimalish): Decimal;
    // (undocumented)
    toString(precision?: number): string;
    // (undocumented)
    static readonly ZERO: Decimal;
    // (undocumented)
    get zero(): this | undefined;
}

// @public
export type Decimalish = Decimal | number | string;

// @alpha (undocumented)
export class Difference {
    // (undocumented)
    get absoluteValue(): Decimal | undefined;
    // (undocumented)
    static between(d1: Decimalish | undefined, d2: Decimalish | undefined): Difference;
    // (undocumented)
    get finite(): this | undefined;
    // (undocumented)
    get infinite(): this | undefined;
    // (undocumented)
    mul(multiplier: Decimalish): Difference;
    // (undocumented)
    get negative(): this | undefined;
    // (undocumented)
    get nonZero(): this | undefined;
    // (undocumented)
    get positive(): this | undefined;
    // (undocumented)
    prettify(precision?: number): string;
    // (undocumented)
    toString(precision?: number): string;
}

// @internal (undocumented)
export const _emptyVault: Vault;

// @public
export type FailedReceipt<R = unknown> = {
    status: "failed";
    rawReceipt: R;
};

// @internal (undocumented)
export const _failedReceipt: <R>(rawReceipt: R) => FailedReceipt<R>;

// @public
export class Fees {
    // @internal
    constructor(baseRateWithoutDecay: Decimalish, minuteDecayFactor: Decimalish, beta: Decimalish, lastFeeOperation: Date, timeOfLatestBlock: Date, recoveryMode: boolean);
    // @internal (undocumented)
    baseRate(when?: Date): Decimal;
    borrowingRate(when?: Date): Decimal;
    equals(that: Fees): boolean;
    redemptionRate(redeemedFractionOfSupply?: Decimalish, when?: Date): Decimal;
    // @internal (undocumented)
    _setRecoveryMode(recoveryMode: boolean): Fees;
    // @internal (undocumented)
    toString(): string;
}

// @public
export type FrontendStatus = {
    status: "unregistered";
} | {
    status: "registered";
    kickbackRate: Decimal;
};

// @public
export interface LiquidationDetails {
    bpdGasCompensation: Decimal;
    collateralGasCompensation: Decimal;
    liquidatedAddresses: string[];
    totalLiquidated: Vault;
}

// @public
export const MAXIMUM_BORROWING_RATE: Decimal;

// @public
export type MinedReceipt<R = unknown, D = unknown> = FailedReceipt<R> | SuccessfulReceipt<R, D>;

// @public
export const MINIMUM_BORROWING_RATE: Decimal;

// @public
export const MINIMUM_COLLATERAL_RATIO: Decimal;

// @public
export const MINIMUM_REDEMPTION_RATE: Decimal;

// @internal (undocumented)
export interface _MoneypReadCache<T extends unknown[]> extends _MoneypReadCacheBase<T> {
    // (undocumented)
    getVaults(params: VaultListingParams & {
        beforeRedistribution: true;
    }, ...extraParams: T): VaultWithPendingRedistribution[] | undefined;
    // (undocumented)
    getVaults(params: VaultListingParams, ...extraParams: T): UserVault[] | undefined;
}

// @internal (undocumented)
export type _MoneypReadCacheBase<T extends unknown[]> = {
    [P in keyof ReadableMoneyp]: ReadableMoneyp[P] extends (...args: infer A) => Promise<infer R> ? (...params: [...originalParams: A, ...extraParams: T]) => R | undefined : never;
};

// @public
export type MoneypReceipt<R = unknown, D = unknown> = PendingReceipt | MinedReceipt<R, D>;

// @public
export abstract class MoneypStore<T = unknown> {
    // @internal (undocumented)
    protected abstract _doStart(): () => void;
    // @internal (undocumented)
    protected _load(baseState: MoneypStoreBaseState, extraState?: T): void;
    // @internal (undocumented)
    protected _loaded: boolean;
    logging: boolean;
    onLoaded?: () => void;
    // @internal (undocumented)
    protected abstract _reduceExtra(extraState: T, extraStateUpdate: Partial<T>): T;
    start(): () => void;
    get state(): MoneypStoreState<T>;
    subscribe(listener: (params: MoneypStoreListenerParams<T>) => void): () => void;
    // @internal (undocumented)
    protected _update(baseStateUpdate?: Partial<MoneypStoreBaseState>, extraStateUpdate?: Partial<T>): void;
    }

// @public
export interface MoneypStoreBaseState {
    accountBalance: Decimal;
    bpdBalance: Decimal;
    bpdInStabilityPool: Decimal;
    collateralSurplusBalance: Decimal;
    // @internal (undocumented)
    _feesInNormalMode: Fees;
    frontend: FrontendStatus;
    liquidityMiningMPReward: Decimal;
    liquidityMiningStake: Decimal;
    mpBalance: Decimal;
    mpStake: MPStake;
    numberOfVaults: number;
    ownFrontend: FrontendStatus;
    price: Decimal;
    remainingLiquidityMiningMPReward: Decimal;
    remainingStabilityPoolMPReward: Decimal;
    // @internal (undocumented)
    _riskiestVaultBeforeRedistribution: VaultWithPendingRedistribution;
    rskSwapTokenAllowance: Decimal;
    rskSwapTokenBalance: Decimal;
    stabilityDeposit: StabilityDeposit;
    total: Vault;
    totalRedistributed: Vault;
    totalStakedMP: Decimal;
    totalStakedRskSwapTokens: Decimal;
    vaultBeforeRedistribution: VaultWithPendingRedistribution;
}

// @public
export interface MoneypStoreDerivedState {
    borrowingRate: Decimal;
    fees: Fees;
    haveUndercollateralizedVaults: boolean;
    redemptionRate: Decimal;
    vault: UserVault;
}

// @public
export interface MoneypStoreListenerParams<T = unknown> {
    newState: MoneypStoreState<T>;
    oldState: MoneypStoreState<T>;
    stateChange: Partial<MoneypStoreState<T>>;
}

// @public
export type MoneypStoreState<T = unknown> = MoneypStoreBaseState & MoneypStoreDerivedState & T;

// @public
export class MPStake {
    // @internal
    constructor(stakedMP?: Decimal, collateralGain?: Decimal, bpdGain?: Decimal);
    apply(change: MPStakeChange<Decimalish> | undefined): Decimal;
    readonly bpdGain: Decimal;
    readonly collateralGain: Decimal;
    equals(that: MPStake): boolean;
    // (undocumented)
    get isEmpty(): boolean;
    readonly stakedMP: Decimal;
    // @internal (undocumented)
    toString(): string;
    whatChanged(thatStakedMP: Decimalish): MPStakeChange<Decimal> | undefined;
}

// @public
export type MPStakeChange<T> = {
    stakeMP: T;
    unstakeMP?: undefined;
} | {
    stakeMP?: undefined;
    unstakeMP: T;
    unstakeAllMP: boolean;
};

// @internal (undocumented)
export type _NoBPDBorrowing = Partial<_BPDBorrowing<undefined>>;

// @internal (undocumented)
export type _NoBPDRepayment = Partial<_BPDRepayment<undefined>>;

// @internal (undocumented)
export type _NoCollateralChange = _NoCollateralDeposit & _NoCollateralWithdrawal;

// @internal (undocumented)
export type _NoCollateralDeposit = Partial<_CollateralDeposit<undefined>>;

// @internal (undocumented)
export type _NoCollateralWithdrawal = Partial<_CollateralWithdrawal<undefined>>;

// @internal (undocumented)
export type _NoDebtChange = _NoBPDBorrowing & _NoBPDRepayment;

// @internal (undocumented)
export const _normalizeVaultAdjustment: (params: Record<string, Decimalish | undefined>) => VaultAdjustmentParams<Decimal>;

// @internal (undocumented)
export const _normalizeVaultCreation: (params: Record<string, Decimalish | undefined>) => VaultCreationParams<Decimal>;

// @alpha (undocumented)
export interface ObservableMoneyp {
    // (undocumented)
    watchBPDBalance(onBPDBalanceChanged: (balance: Decimal) => void, address?: string): () => void;
    // (undocumented)
    watchBPDInStabilityPool(onBPDInStabilityPoolChanged: (bpdInStabilityPool: Decimal) => void): () => void;
    // (undocumented)
    watchNumberOfVaults(onNumberOfVaultsChanged: (numberOfVaults: number) => void): () => void;
    // (undocumented)
    watchPrice(onPriceChanged: (price: Decimal) => void): () => void;
    // (undocumented)
    watchStabilityDeposit(onStabilityDepositChanged: (stabilityDeposit: StabilityDeposit) => void, address?: string): () => void;
    // (undocumented)
    watchTotal(onTotalChanged: (total: Vault) => void): () => void;
    // (undocumented)
    watchTotalRedistributed(onTotalRedistributedChanged: (totalRedistributed: Vault) => void): () => void;
    // (undocumented)
    watchVaultWithoutRewards(onVaultChanged: (vault: VaultWithPendingRedistribution) => void, address?: string): () => void;
}

// @public
export type PendingReceipt = {
    status: "pending";
};

// @internal (undocumented)
export const _pendingReceipt: PendingReceipt;

// @alpha (undocumented)
export class Percent<T extends {
    infinite?: T | undefined;
    absoluteValue?: A | undefined;
    mul?(hundred: 100): T;
    toString(precision?: number): string;
}, A extends {
    gte(n: string): boolean;
}> {
    constructor(ratio: T);
    // (undocumented)
    nonZeroish(precision: number): this | undefined;
    // (undocumented)
    prettify(): string;
    // (undocumented)
    toString(precision: number): string;
}

// @internal (undocumented)
export type _PopulatableFrom<T, P> = {
    [M in keyof T]: T[M] extends (...args: infer A) => Promise<infer U> ? U extends SentMoneypTransaction ? (...args: A) => Promise<PopulatedMoneypTransaction<P, U>> : never : never;
};

// Warning: (ae-incompatible-release-tags) The symbol "PopulatableMoneyp" is marked as @public, but its signature references "_PopulatableFrom" which is marked as @internal
//
// @public
export interface PopulatableMoneyp<R = unknown, S = unknown, P = unknown> extends _PopulatableFrom<SendableMoneyp<R, S>, P> {
    adjustVault(params: VaultAdjustmentParams<Decimalish>, maxBorrowingRate?: Decimalish): Promise<PopulatedMoneypTransaction<P, SentMoneypTransaction<S, MoneypReceipt<R, VaultAdjustmentDetails>>>>;
    approveRskSwapTokens(allowance?: Decimalish): Promise<PopulatedMoneypTransaction<P, SentMoneypTransaction<S, MoneypReceipt<R, void>>>>;
    borrowBPD(amount: Decimalish, maxBorrowingRate?: Decimalish): Promise<PopulatedMoneypTransaction<P, SentMoneypTransaction<S, MoneypReceipt<R, VaultAdjustmentDetails>>>>;
    claimCollateralSurplus(): Promise<PopulatedMoneypTransaction<P, SentMoneypTransaction<S, MoneypReceipt<R, void>>>>;
    closeVault(): Promise<PopulatedMoneypTransaction<P, SentMoneypTransaction<S, MoneypReceipt<R, VaultClosureDetails>>>>;
    depositBPDInStabilityPool(amount: Decimalish, frontendTag?: string): Promise<PopulatedMoneypTransaction<P, SentMoneypTransaction<S, MoneypReceipt<R, StabilityDepositChangeDetails>>>>;
    depositCollateral(amount: Decimalish): Promise<PopulatedMoneypTransaction<P, SentMoneypTransaction<S, MoneypReceipt<R, VaultAdjustmentDetails>>>>;
    exitLiquidityMining(): Promise<PopulatedMoneypTransaction<P, SentMoneypTransaction<S, MoneypReceipt<R, void>>>>;
    liquidate(address: string | string[]): Promise<PopulatedMoneypTransaction<P, SentMoneypTransaction<S, MoneypReceipt<R, LiquidationDetails>>>>;
    liquidateUpTo(maximumNumberOfVaultsToLiquidate: number): Promise<PopulatedMoneypTransaction<P, SentMoneypTransaction<S, MoneypReceipt<R, LiquidationDetails>>>>;
    openVault(params: VaultCreationParams<Decimalish>, maxBorrowingRate?: Decimalish): Promise<PopulatedMoneypTransaction<P, SentMoneypTransaction<S, MoneypReceipt<R, VaultCreationDetails>>>>;
    redeemBPD(amount: Decimalish, maxRedemptionRate?: Decimalish): Promise<PopulatedRedemption<P, S, R>>;
    registerFrontend(kickbackRate: Decimalish): Promise<PopulatedMoneypTransaction<P, SentMoneypTransaction<S, MoneypReceipt<R, void>>>>;
    repayBPD(amount: Decimalish): Promise<PopulatedMoneypTransaction<P, SentMoneypTransaction<S, MoneypReceipt<R, VaultAdjustmentDetails>>>>;
    sendBPD(toAddress: string, amount: Decimalish): Promise<PopulatedMoneypTransaction<P, SentMoneypTransaction<S, MoneypReceipt<R, void>>>>;
    sendMP(toAddress: string, amount: Decimalish): Promise<PopulatedMoneypTransaction<P, SentMoneypTransaction<S, MoneypReceipt<R, void>>>>;
    // @internal (undocumented)
    setPrice(price: Decimalish): Promise<PopulatedMoneypTransaction<P, SentMoneypTransaction<S, MoneypReceipt<R, void>>>>;
    stakeMP(amount: Decimalish): Promise<PopulatedMoneypTransaction<P, SentMoneypTransaction<S, MoneypReceipt<R, void>>>>;
    stakeRskSwapTokens(amount: Decimalish): Promise<PopulatedMoneypTransaction<P, SentMoneypTransaction<S, MoneypReceipt<R, void>>>>;
    transferCollateralGainToVault(): Promise<PopulatedMoneypTransaction<P, SentMoneypTransaction<S, MoneypReceipt<R, CollateralGainTransferDetails>>>>;
    unstakeMP(amount: Decimalish): Promise<PopulatedMoneypTransaction<P, SentMoneypTransaction<S, MoneypReceipt<R, void>>>>;
    unstakeRskSwapTokens(amount: Decimalish): Promise<PopulatedMoneypTransaction<P, SentMoneypTransaction<S, MoneypReceipt<R, void>>>>;
    withdrawBPDFromStabilityPool(amount: Decimalish): Promise<PopulatedMoneypTransaction<P, SentMoneypTransaction<S, MoneypReceipt<R, StabilityDepositChangeDetails>>>>;
    withdrawCollateral(amount: Decimalish): Promise<PopulatedMoneypTransaction<P, SentMoneypTransaction<S, MoneypReceipt<R, VaultAdjustmentDetails>>>>;
    withdrawGainsFromStabilityPool(): Promise<PopulatedMoneypTransaction<P, SentMoneypTransaction<S, MoneypReceipt<R, StabilityPoolGainsWithdrawalDetails>>>>;
    withdrawGainsFromStaking(): Promise<PopulatedMoneypTransaction<P, SentMoneypTransaction<S, MoneypReceipt<R, void>>>>;
    withdrawMPRewardFromLiquidityMining(): Promise<PopulatedMoneypTransaction<P, SentMoneypTransaction<S, MoneypReceipt<R, void>>>>;
}

// @public
export interface PopulatedMoneypTransaction<P = unknown, T extends SentMoneypTransaction = SentMoneypTransaction> {
    readonly rawPopulatedTransaction: P;
    send(): Promise<T>;
}

// @public
export interface PopulatedRedemption<P = unknown, S = unknown, R = unknown> extends PopulatedMoneypTransaction<P, SentMoneypTransaction<S, MoneypReceipt<R, RedemptionDetails>>> {
    readonly attemptedBPDAmount: Decimal;
    increaseAmountByMinimumNetDebt(maxRedemptionRate?: Decimalish): Promise<PopulatedRedemption<P, S, R>>;
    readonly isTruncated: boolean;
    readonly redeemableBPDAmount: Decimal;
}

// @public
export interface ReadableMoneyp {
    getBPDBalance(address?: string): Promise<Decimal>;
    getBPDInStabilityPool(): Promise<Decimal>;
    getCollateralSurplusBalance(address?: string): Promise<Decimal>;
    getFees(): Promise<Fees>;
    getFrontendStatus(address?: string): Promise<FrontendStatus>;
    getLiquidityMiningMPReward(address?: string): Promise<Decimal>;
    getLiquidityMiningStake(address?: string): Promise<Decimal>;
    getMPBalance(address?: string): Promise<Decimal>;
    getMPStake(address?: string): Promise<MPStake>;
    getNumberOfVaults(): Promise<number>;
    getPrice(): Promise<Decimal>;
    getRemainingLiquidityMiningMPReward(): Promise<Decimal>;
    getRemainingStabilityPoolMPReward(): Promise<Decimal>;
    getRskSwapTokenAllowance(address?: string): Promise<Decimal>;
    getRskSwapTokenBalance(address?: string): Promise<Decimal>;
    getStabilityDeposit(address?: string): Promise<StabilityDeposit>;
    getTotal(): Promise<Vault>;
    getTotalRedistributed(): Promise<Vault>;
    getTotalStakedMP(): Promise<Decimal>;
    getTotalStakedRskSwapTokens(): Promise<Decimal>;
    getVault(address?: string): Promise<UserVault>;
    getVaultBeforeRedistribution(address?: string): Promise<VaultWithPendingRedistribution>;
    // @internal (undocumented)
    getVaults(params: VaultListingParams & {
        beforeRedistribution: true;
    }): Promise<VaultWithPendingRedistribution[]>;
    getVaults(params: VaultListingParams): Promise<UserVault[]>;
}

// @internal (undocumented)
export interface _ReadableMoneypWithExtraParams<T extends unknown[]> extends _ReadableMoneypWithExtraParamsBase<T> {
    // (undocumented)
    getVaults(params: VaultListingParams & {
        beforeRedistribution: true;
    }, ...extraParams: T): Promise<VaultWithPendingRedistribution[]>;
    // (undocumented)
    getVaults(params: VaultListingParams, ...extraParams: T): Promise<UserVault[]>;
}

// @internal (undocumented)
export type _ReadableMoneypWithExtraParamsBase<T extends unknown[]> = {
    [P in keyof ReadableMoneyp]: ReadableMoneyp[P] extends (...params: infer A) => infer R ? (...params: [...originalParams: A, ...extraParams: T]) => R : never;
};

// @public
export interface RedemptionDetails {
    actualBPDAmount: Decimal;
    attemptedBPDAmount: Decimal;
    collateralTaken: Decimal;
    fee: Decimal;
}

// @internal (undocumented)
export type _SendableFrom<T, R, S> = {
    [M in keyof T]: T[M] extends (...args: infer A) => Promise<infer D> ? (...args: A) => Promise<SentMoneypTransaction<S, MoneypReceipt<R, D>>> : never;
};

// Warning: (ae-incompatible-release-tags) The symbol "SendableMoneyp" is marked as @public, but its signature references "_SendableFrom" which is marked as @internal
//
// @public
export interface SendableMoneyp<R = unknown, S = unknown> extends _SendableFrom<TransactableMoneyp, R, S> {
    adjustVault(params: VaultAdjustmentParams<Decimalish>, maxBorrowingRate?: Decimalish): Promise<SentMoneypTransaction<S, MoneypReceipt<R, VaultAdjustmentDetails>>>;
    approveRskSwapTokens(allowance?: Decimalish): Promise<SentMoneypTransaction<S, MoneypReceipt<R, void>>>;
    borrowBPD(amount: Decimalish, maxBorrowingRate?: Decimalish): Promise<SentMoneypTransaction<S, MoneypReceipt<R, VaultAdjustmentDetails>>>;
    claimCollateralSurplus(): Promise<SentMoneypTransaction<S, MoneypReceipt<R, void>>>;
    closeVault(): Promise<SentMoneypTransaction<S, MoneypReceipt<R, VaultClosureDetails>>>;
    depositBPDInStabilityPool(amount: Decimalish, frontendTag?: string): Promise<SentMoneypTransaction<S, MoneypReceipt<R, StabilityDepositChangeDetails>>>;
    depositCollateral(amount: Decimalish): Promise<SentMoneypTransaction<S, MoneypReceipt<R, VaultAdjustmentDetails>>>;
    exitLiquidityMining(): Promise<SentMoneypTransaction<S, MoneypReceipt<R, void>>>;
    liquidate(address: string | string[]): Promise<SentMoneypTransaction<S, MoneypReceipt<R, LiquidationDetails>>>;
    liquidateUpTo(maximumNumberOfVaultsToLiquidate: number): Promise<SentMoneypTransaction<S, MoneypReceipt<R, LiquidationDetails>>>;
    openVault(params: VaultCreationParams<Decimalish>, maxBorrowingRate?: Decimalish): Promise<SentMoneypTransaction<S, MoneypReceipt<R, VaultCreationDetails>>>;
    redeemBPD(amount: Decimalish, maxRedemptionRate?: Decimalish): Promise<SentMoneypTransaction<S, MoneypReceipt<R, RedemptionDetails>>>;
    registerFrontend(kickbackRate: Decimalish): Promise<SentMoneypTransaction<S, MoneypReceipt<R, void>>>;
    repayBPD(amount: Decimalish): Promise<SentMoneypTransaction<S, MoneypReceipt<R, VaultAdjustmentDetails>>>;
    sendBPD(toAddress: string, amount: Decimalish): Promise<SentMoneypTransaction<S, MoneypReceipt<R, void>>>;
    sendMP(toAddress: string, amount: Decimalish): Promise<SentMoneypTransaction<S, MoneypReceipt<R, void>>>;
    // @internal (undocumented)
    setPrice(price: Decimalish): Promise<SentMoneypTransaction<S, MoneypReceipt<R, void>>>;
    stakeMP(amount: Decimalish): Promise<SentMoneypTransaction<S, MoneypReceipt<R, void>>>;
    stakeRskSwapTokens(amount: Decimalish): Promise<SentMoneypTransaction<S, MoneypReceipt<R, void>>>;
    transferCollateralGainToVault(): Promise<SentMoneypTransaction<S, MoneypReceipt<R, CollateralGainTransferDetails>>>;
    unstakeMP(amount: Decimalish): Promise<SentMoneypTransaction<S, MoneypReceipt<R, void>>>;
    unstakeRskSwapTokens(amount: Decimalish): Promise<SentMoneypTransaction<S, MoneypReceipt<R, void>>>;
    withdrawBPDFromStabilityPool(amount: Decimalish): Promise<SentMoneypTransaction<S, MoneypReceipt<R, StabilityDepositChangeDetails>>>;
    withdrawCollateral(amount: Decimalish): Promise<SentMoneypTransaction<S, MoneypReceipt<R, VaultAdjustmentDetails>>>;
    withdrawGainsFromStabilityPool(): Promise<SentMoneypTransaction<S, MoneypReceipt<R, StabilityPoolGainsWithdrawalDetails>>>;
    withdrawGainsFromStaking(): Promise<SentMoneypTransaction<S, MoneypReceipt<R, void>>>;
    withdrawMPRewardFromLiquidityMining(): Promise<SentMoneypTransaction<S, MoneypReceipt<R, void>>>;
}

// @public
export interface SentMoneypTransaction<S = unknown, T extends MoneypReceipt = MoneypReceipt> {
    getReceipt(): Promise<T>;
    readonly rawSentTransaction: S;
    waitForReceipt(): Promise<Extract<T, MinedReceipt>>;
}

// @public
export class StabilityDeposit {
    // @internal
    constructor(initialBPD: Decimal, currentBPD: Decimal, collateralGain: Decimal, mpReward: Decimal, frontendTag: string);
    apply(change: StabilityDepositChange<Decimalish> | undefined): Decimal;
    readonly collateralGain: Decimal;
    readonly currentBPD: Decimal;
    equals(that: StabilityDeposit): boolean;
    readonly frontendTag: string;
    readonly initialBPD: Decimal;
    // (undocumented)
    get isEmpty(): boolean;
    readonly mpReward: Decimal;
    // @internal (undocumented)
    toString(): string;
    whatChanged(thatBPD: Decimalish): StabilityDepositChange<Decimal> | undefined;
}

// @public
export type StabilityDepositChange<T> = {
    depositBPD: T;
    withdrawBPD?: undefined;
} | {
    depositBPD?: undefined;
    withdrawBPD: T;
    withdrawAllBPD: boolean;
};

// @public
export interface StabilityDepositChangeDetails extends StabilityPoolGainsWithdrawalDetails {
    change: StabilityDepositChange<Decimal>;
}

// @public
export interface StabilityPoolGainsWithdrawalDetails {
    bpdLoss: Decimal;
    collateralGain: Decimal;
    mpReward: Decimal;
    newBPDDeposit: Decimal;
}

// @public
export type SuccessfulReceipt<R = unknown, D = unknown> = {
    status: "succeeded";
    rawReceipt: R;
    details: D;
};

// @internal (undocumented)
export const _successfulReceipt: <R, D>(rawReceipt: R, details: D, toString?: (() => string) | undefined) => SuccessfulReceipt<R, D>;

// @public
export interface TransactableMoneyp {
    adjustVault(params: VaultAdjustmentParams<Decimalish>, maxBorrowingRate?: Decimalish): Promise<VaultAdjustmentDetails>;
    approveRskSwapTokens(allowance?: Decimalish): Promise<void>;
    borrowBPD(amount: Decimalish, maxBorrowingRate?: Decimalish): Promise<VaultAdjustmentDetails>;
    claimCollateralSurplus(): Promise<void>;
    closeVault(): Promise<VaultClosureDetails>;
    depositBPDInStabilityPool(amount: Decimalish, frontendTag?: string): Promise<StabilityDepositChangeDetails>;
    depositCollateral(amount: Decimalish): Promise<VaultAdjustmentDetails>;
    exitLiquidityMining(): Promise<void>;
    liquidate(address: string | string[]): Promise<LiquidationDetails>;
    liquidateUpTo(maximumNumberOfVaultsToLiquidate: number): Promise<LiquidationDetails>;
    openVault(params: VaultCreationParams<Decimalish>, maxBorrowingRate?: Decimalish): Promise<VaultCreationDetails>;
    redeemBPD(amount: Decimalish, maxRedemptionRate?: Decimalish): Promise<RedemptionDetails>;
    registerFrontend(kickbackRate: Decimalish): Promise<void>;
    repayBPD(amount: Decimalish): Promise<VaultAdjustmentDetails>;
    sendBPD(toAddress: string, amount: Decimalish): Promise<void>;
    sendMP(toAddress: string, amount: Decimalish): Promise<void>;
    // @internal (undocumented)
    setPrice(price: Decimalish): Promise<void>;
    stakeMP(amount: Decimalish): Promise<void>;
    stakeRskSwapTokens(amount: Decimalish): Promise<void>;
    transferCollateralGainToVault(): Promise<CollateralGainTransferDetails>;
    unstakeMP(amount: Decimalish): Promise<void>;
    unstakeRskSwapTokens(amount: Decimalish): Promise<void>;
    withdrawBPDFromStabilityPool(amount: Decimalish): Promise<StabilityDepositChangeDetails>;
    withdrawCollateral(amount: Decimalish): Promise<VaultAdjustmentDetails>;
    withdrawGainsFromStabilityPool(): Promise<StabilityPoolGainsWithdrawalDetails>;
    withdrawGainsFromStaking(): Promise<void>;
    withdrawMPRewardFromLiquidityMining(): Promise<void>;
}

// @public
export class TransactionFailedError<T extends FailedReceipt = FailedReceipt> extends Error {
    // @internal
    constructor(name: string, message: string, failedReceipt: T);
    // (undocumented)
    readonly failedReceipt: T;
}

// @public
export class UserVault extends Vault {
    // @internal
    constructor(ownerAddress: string, status: UserVaultStatus, collateral?: Decimal, debt?: Decimal);
    // (undocumented)
    equals(that: UserVault): boolean;
    readonly ownerAddress: string;
    readonly status: UserVaultStatus;
    // @internal (undocumented)
    toString(): string;
}

// @public
export type UserVaultStatus = "nonExistent" | "open" | "closedByOwner" | "closedByLiquidation" | "closedByRedemption";

// @public
export class Vault {
    // @internal
    constructor(collateral?: Decimal, debt?: Decimal);
    // (undocumented)
    add(that: Vault): Vault;
    // (undocumented)
    addCollateral(collateral: Decimalish): Vault;
    // (undocumented)
    addDebt(debt: Decimalish): Vault;
    adjust(params: VaultAdjustmentParams<Decimalish>, borrowingRate?: Decimalish): Vault;
    adjustTo(that: Vault, borrowingRate?: Decimalish): VaultAdjustmentParams<Decimal>;
    apply(change: VaultChange<Decimal> | undefined, borrowingRate?: Decimalish): Vault;
    readonly collateral: Decimal;
    collateralRatio(price: Decimalish): Decimal;
    collateralRatioIsBelowCritical(price: Decimalish): boolean;
    collateralRatioIsBelowMinimum(price: Decimalish): boolean;
    static create(params: VaultCreationParams<Decimalish>, borrowingRate?: Decimalish): Vault;
    readonly debt: Decimal;
    // (undocumented)
    equals(that: Vault): boolean;
    // (undocumented)
    get isEmpty(): boolean;
    isOpenableInRecoveryMode(price: Decimalish): boolean;
    // (undocumented)
    multiply(multiplier: Decimalish): Vault;
    get netDebt(): Decimal;
    // @internal (undocumented)
    get _nominalCollateralRatio(): Decimal;
    static recreate(that: Vault, borrowingRate?: Decimalish): VaultCreationParams<Decimal>;
    // (undocumented)
    setCollateral(collateral: Decimalish): Vault;
    // (undocumented)
    setDebt(debt: Decimalish): Vault;
    // (undocumented)
    subtract(that: Vault): Vault;
    // (undocumented)
    subtractCollateral(collateral: Decimalish): Vault;
    // (undocumented)
    subtractDebt(debt: Decimalish): Vault;
    // @internal (undocumented)
    toString(): string;
    whatChanged(that: Vault, borrowingRate?: Decimalish): VaultChange<Decimal> | undefined;
}

// @public
export interface VaultAdjustmentDetails {
    fee: Decimal;
    newVault: Vault;
    params: VaultAdjustmentParams<Decimal>;
}

// Warning: (ae-incompatible-release-tags) The symbol "VaultAdjustmentParams" is marked as @public, but its signature references "_CollateralChange" which is marked as @internal
// Warning: (ae-incompatible-release-tags) The symbol "VaultAdjustmentParams" is marked as @public, but its signature references "_NoDebtChange" which is marked as @internal
// Warning: (ae-incompatible-release-tags) The symbol "VaultAdjustmentParams" is marked as @public, but its signature references "_DebtChange" which is marked as @internal
// Warning: (ae-incompatible-release-tags) The symbol "VaultAdjustmentParams" is marked as @public, but its signature references "_NoCollateralChange" which is marked as @internal
//
// @public
export type VaultAdjustmentParams<T = unknown> = (_CollateralChange<T> & _NoDebtChange) | (_DebtChange<T> & _NoCollateralChange) | (_CollateralChange<T> & _DebtChange<T>);

// @public
export type VaultChange<T> = {
    type: "invalidCreation";
    invalidVault: Vault;
    error: VaultCreationError;
} | {
    type: "creation";
    params: VaultCreationParams<T>;
} | {
    type: "closure";
    params: VaultClosureParams<T>;
} | {
    type: "adjustment";
    params: VaultAdjustmentParams<T>;
    setToZero?: "collateral" | "debt";
};

// @public
export interface VaultClosureDetails {
    params: VaultClosureParams<Decimal>;
}

// Warning: (ae-incompatible-release-tags) The symbol "VaultClosureParams" is marked as @public, but its signature references "_CollateralWithdrawal" which is marked as @internal
// Warning: (ae-incompatible-release-tags) The symbol "VaultClosureParams" is marked as @public, but its signature references "_NoCollateralDeposit" which is marked as @internal
// Warning: (ae-incompatible-release-tags) The symbol "VaultClosureParams" is marked as @public, but its signature references "_BPDRepayment" which is marked as @internal
// Warning: (ae-incompatible-release-tags) The symbol "VaultClosureParams" is marked as @public, but its signature references "_NoBPDBorrowing" which is marked as @internal
//
// @public
export type VaultClosureParams<T> = _CollateralWithdrawal<T> & _NoCollateralDeposit & Partial<_BPDRepayment<T>> & _NoBPDBorrowing;

// @public
export interface VaultCreationDetails {
    fee: Decimal;
    newVault: Vault;
    params: VaultCreationParams<Decimal>;
}

// @public
export type VaultCreationError = "missingLiquidationReserve";

// Warning: (ae-incompatible-release-tags) The symbol "VaultCreationParams" is marked as @public, but its signature references "_CollateralDeposit" which is marked as @internal
// Warning: (ae-incompatible-release-tags) The symbol "VaultCreationParams" is marked as @public, but its signature references "_NoCollateralWithdrawal" which is marked as @internal
// Warning: (ae-incompatible-release-tags) The symbol "VaultCreationParams" is marked as @public, but its signature references "_BPDBorrowing" which is marked as @internal
// Warning: (ae-incompatible-release-tags) The symbol "VaultCreationParams" is marked as @public, but its signature references "_NoBPDRepayment" which is marked as @internal
//
// @public
export type VaultCreationParams<T = unknown> = _CollateralDeposit<T> & _NoCollateralWithdrawal & _BPDBorrowing<T> & _NoBPDRepayment;

// @public
export interface VaultListingParams {
    readonly beforeRedistribution?: boolean;
    readonly first: number;
    readonly sortedBy: "ascendingCollateralRatio" | "descendingCollateralRatio";
    readonly startingAt?: number;
}

// @public
export class VaultWithPendingRedistribution extends UserVault {
    // @internal
    constructor(ownerAddress: string, status: UserVaultStatus, collateral?: Decimal, debt?: Decimal, stake?: Decimal, snapshotOfTotalRedistributed?: Vault);
    // (undocumented)
    applyRedistribution(totalRedistributed: Vault): UserVault;
    // (undocumented)
    equals(that: VaultWithPendingRedistribution): boolean;
    }


// (No @packageDocumentation comment for this package)

```
